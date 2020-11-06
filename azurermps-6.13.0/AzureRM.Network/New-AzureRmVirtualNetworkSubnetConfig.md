---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494042"
---
# <span data-ttu-id="6b2fd-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fd-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="6b2fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2fd-103">Virtuális hálózati alhálózat-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b2fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b2fd-104">SYNTAX</span></span>

### <span data-ttu-id="6b2fd-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b2fd-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b2fd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b2fd-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b2fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b2fd-107">DESCRIPTION</span></span>
<span data-ttu-id="6b2fd-108">**A New-AzureRmVirtualNetworkSubnetConfig** parancsmag virtuális hálózati alhálózat-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="6b2fd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6b2fd-109">EXAMPLES</span></span>

### <span data-ttu-id="6b2fd-110">1: virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="6b2fd-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="6b2fd-111">Ez a példa két új alhálózat-konfigurációt hoz létre az New-AzureRmVirtualSubnetConfig parancsmag segítségével, majd virtuális hálózat létrehozására használja őket.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="6b2fd-112">A New-AzureRmVirtualSubnetConfig sablon csak az alhálózat memória szerinti ábrázolását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="6b2fd-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24 verzióval rendelkezik, és egy hálózati biztonsági csoportra hivatkozik, amely lehetővé teszi az RDP-hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="6b2fd-114">A backendSubnet CIDR 10.0.2.0/24 verzióval rendelkezik, és ugyanarra a hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="6b2fd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b2fd-115">PARAMETERS</span></span>

### <span data-ttu-id="6b2fd-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6b2fd-116">-AddressPrefix</span></span>
<span data-ttu-id="6b2fd-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="6b2fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2fd-118">-DefaultProfile</span></span>
<span data-ttu-id="6b2fd-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b2fd-120">– Meghatalmazás</span><span class="sxs-lookup"><span data-stu-id="6b2fd-120">-Delegation</span></span>
<span data-ttu-id="6b2fd-121">Azon szolgáltatások listája, amelyeken műveleteket végezhet el az alhálózatban.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="6b2fd-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6b2fd-122">-Name</span></span>
<span data-ttu-id="6b2fd-123">A létrehozandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="6b2fd-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b2fd-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="6b2fd-125">Egy NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="6b2fd-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6b2fd-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6b2fd-127">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="6b2fd-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="6b2fd-128">-RouteTable</span></span>
<span data-ttu-id="6b2fd-129">Az alhálózati konfigurációhoz társított útvonal táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="6b2fd-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="6b2fd-130">-RouteTableId</span></span>
<span data-ttu-id="6b2fd-131">Az alhálózati konfigurációhoz társított útvonali táblázat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6b2fd-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="6b2fd-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b2fd-132">-ServiceEndpoint</span></span>
<span data-ttu-id="6b2fd-133">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="6b2fd-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="6b2fd-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="6b2fd-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="6b2fd-135">Szolgáltatási végpontokra vonatkozó házirendek</span><span class="sxs-lookup"><span data-stu-id="6b2fd-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="6b2fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2fd-136">CommonParameters</span></span>
<span data-ttu-id="6b2fd-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b2fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2fd-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2fd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2fd-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b2fd-139">INPUTS</span></span>

### <span data-ttu-id="6b2fd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6b2fd-140">System.String</span></span>

### <span data-ttu-id="6b2fd-141">Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b2fd-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="6b2fd-142">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b2fd-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="6b2fd-143">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b2fd-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6b2fd-144">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSServiceEndpointPolicy, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6b2fd-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6b2fd-145">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. commands. Network, Version = 6.7.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6b2fd-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b2fd-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b2fd-146">OUTPUTS</span></span>

### <span data-ttu-id="6b2fd-147">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6b2fd-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="6b2fd-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b2fd-148">NOTES</span></span>

## <span data-ttu-id="6b2fd-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b2fd-149">RELATED LINKS</span></span>

[<span data-ttu-id="6b2fd-150">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fd-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6b2fd-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fd-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6b2fd-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fd-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6b2fd-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fd-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


