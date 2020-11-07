---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841245"
---
# <span data-ttu-id="0c3ff-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c3ff-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="0c3ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3ff-103">Virtuális hálózati alhálózat-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="0c3ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c3ff-104">SYNTAX</span></span>

### <span data-ttu-id="0c3ff-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c3ff-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c3ff-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c3ff-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c3ff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c3ff-107">DESCRIPTION</span></span>
<span data-ttu-id="0c3ff-108">**A New-AzVirtualNetworkSubnetConfig** parancsmag virtuális hálózati alhálózat-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="0c3ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0c3ff-109">EXAMPLES</span></span>

### <span data-ttu-id="0c3ff-110">1: virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="0c3ff-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="0c3ff-111">Ez a példa két új alhálózat-konfigurációt hoz létre az New-AzVirtualSubnetConfig parancsmag segítségével, majd virtuális hálózat létrehozására használja őket.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="0c3ff-112">A New-AzVirtualSubnetConfig sablon csak az alhálózat memória szerinti ábrázolását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="0c3ff-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24 verzióval rendelkezik, és egy hálózati biztonsági csoportra hivatkozik, amely lehetővé teszi az RDP-hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="0c3ff-114">A backendSubnet CIDR 10.0.2.0/24 verzióval rendelkezik, és ugyanarra a hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="0c3ff-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c3ff-115">PARAMETERS</span></span>

### <span data-ttu-id="0c3ff-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0c3ff-116">-AddressPrefix</span></span>
<span data-ttu-id="0c3ff-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3ff-118">-DefaultProfile</span></span>
<span data-ttu-id="0c3ff-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c3ff-120">-Name</span></span>
<span data-ttu-id="0c3ff-121">A létrehozandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-121">Specifies the name of the subnet configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c3ff-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0c3ff-123">Egy NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-123">Specifies a NetworkSecurityGroup object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0c3ff-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="0c3ff-125">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-125">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0c3ff-126">-RouteTable</span></span>
<span data-ttu-id="0c3ff-127">Az alhálózati konfigurációhoz társított útvonal táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-127">Specifies the route table associated with the subnet configuration.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="0c3ff-128">-RouteTableId</span></span>
<span data-ttu-id="0c3ff-129">Az alhálózati konfigurációhoz társított útvonali táblázat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3ff-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ff-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c3ff-130">-ServiceEndpoint</span></span>
<span data-ttu-id="0c3ff-131">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="0c3ff-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="0c3ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3ff-132">CommonParameters</span></span>
<span data-ttu-id="0c3ff-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c3ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3ff-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3ff-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3ff-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3ff-135">INPUTS</span></span>

## <span data-ttu-id="0c3ff-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3ff-136">OUTPUTS</span></span>

### <span data-ttu-id="0c3ff-137">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0c3ff-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="0c3ff-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c3ff-138">NOTES</span></span>

## <span data-ttu-id="0c3ff-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c3ff-139">RELATED LINKS</span></span>

[<span data-ttu-id="0c3ff-140">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c3ff-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c3ff-141">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c3ff-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c3ff-142">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c3ff-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c3ff-143">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c3ff-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


