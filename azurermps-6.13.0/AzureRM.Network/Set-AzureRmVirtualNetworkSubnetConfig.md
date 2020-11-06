---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e8aeb73c694229e290ee96fa11d3de71bb510ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494985"
---
# <span data-ttu-id="684da-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="684da-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="684da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="684da-102">SYNOPSIS</span></span>
<span data-ttu-id="684da-103">Egy virtuális hálózat alhálózat-konfigurációjának cél állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="684da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="684da-104">SYNTAX</span></span>

### <span data-ttu-id="684da-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="684da-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="684da-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="684da-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="684da-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="684da-107">DESCRIPTION</span></span>
<span data-ttu-id="684da-108">A **set-AzureRmVirtualNetworkSubnetConfig** parancsmag a cél állapotát az Azure virtuális hálózatban lévő alhálózati konfigurációhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="684da-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="684da-109">Példák</span><span class="sxs-lookup"><span data-stu-id="684da-109">EXAMPLES</span></span>

### <span data-ttu-id="684da-110">1: az alhálózat cím előtagjának módosítása</span><span class="sxs-lookup"><span data-stu-id="684da-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="684da-111">Ez a példa egy virtuális hálózatot hoz létre egy alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="684da-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="684da-112">Ezután a hívások Set-AzureRmVirtualNetworkSubnetConfig az alhálózat AddressPrefix módosítására.</span><span class="sxs-lookup"><span data-stu-id="684da-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="684da-113">Ez a funkció csak a virtuális hálózat memóriában való megjelenítését befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="684da-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="684da-114">Ezt követően a rendszer az Azure virtuális hálózatának módosítását kéri Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="684da-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="684da-115">2: hálózati biztonsági csoport hozzáadása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="684da-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="684da-116">Ez a példa olyan erőforráscsoportot hoz létre, amelynek egyetlen virtuális hálózata csak egy alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="684da-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="684da-117">Ekkor létrehoz egy hálózati biztonsági csoportot az RDP-forgalom engedélyezési szabályával.</span><span class="sxs-lookup"><span data-stu-id="684da-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="684da-118">A Set-AzureRmVirtualNetworkSubnetConfig parancsmag a felületi alhálózat memóriában való megjelenítésének módosítására szolgál, hogy az az újonnan létrehozott hálózati biztonsági csoportra mutasson.</span><span class="sxs-lookup"><span data-stu-id="684da-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="684da-119">Ezt követően az Set-AzureRmVirtualNetwork parancsmag a módosított állapotnak a szolgáltatásba való visszaírását kéri.</span><span class="sxs-lookup"><span data-stu-id="684da-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="684da-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="684da-120">PARAMETERS</span></span>

### <span data-ttu-id="684da-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="684da-121">-AddressPrefix</span></span>
<span data-ttu-id="684da-122">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="684da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684da-123">-DefaultProfile</span></span>
<span data-ttu-id="684da-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="684da-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="684da-125">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="684da-125">-Delegation</span></span>
<span data-ttu-id="684da-126">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="684da-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="684da-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="684da-127">-Name</span></span>
<span data-ttu-id="684da-128">A parancsmag által konfigurált alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="684da-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="684da-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="684da-130">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="684da-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="684da-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="684da-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="684da-132">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="684da-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="684da-133">-RouteTable</span></span>
<span data-ttu-id="684da-134">A hálózati biztonsági csoporthoz tartozó Route Table objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="684da-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="684da-135">-RouteTableId</span></span>
<span data-ttu-id="684da-136">Annak az útválasztási objektumnak az AZONOSÍTÓját adja meg, amely a hálózat biztonsági csoportjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="684da-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="684da-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="684da-137">-ServiceEndpoint</span></span>
<span data-ttu-id="684da-138">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="684da-138">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="684da-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="684da-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="684da-140">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="684da-140">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="684da-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="684da-141">-VirtualNetwork</span></span>
<span data-ttu-id="684da-142">Az alhálózati konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="684da-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="684da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684da-143">CommonParameters</span></span>
<span data-ttu-id="684da-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="684da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684da-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684da-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684da-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="684da-146">INPUTS</span></span>

### <span data-ttu-id="684da-147">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="684da-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="684da-148">System. String</span><span class="sxs-lookup"><span data-stu-id="684da-148">System.String</span></span>

### <span data-ttu-id="684da-149">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="684da-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="684da-150">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="684da-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="684da-151">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="684da-151">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="684da-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="684da-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="684da-153">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="684da-153">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="684da-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="684da-154">OUTPUTS</span></span>

### <span data-ttu-id="684da-155">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="684da-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="684da-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="684da-156">NOTES</span></span>

## <span data-ttu-id="684da-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="684da-157">RELATED LINKS</span></span>

[<span data-ttu-id="684da-158">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="684da-158">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="684da-159">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="684da-159">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="684da-160">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="684da-160">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="684da-161">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="684da-161">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


