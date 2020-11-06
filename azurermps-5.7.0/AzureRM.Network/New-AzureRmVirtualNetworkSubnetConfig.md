---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: be1b0f81aa33fb0f1368e5730e80f41b9fdcabb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499735"
---
# <span data-ttu-id="ba139-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ba139-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="ba139-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba139-102">SYNOPSIS</span></span>
<span data-ttu-id="ba139-103">Virtuális hálózati alhálózat-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ba139-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba139-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba139-104">SYNTAX</span></span>

### <span data-ttu-id="ba139-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba139-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba139-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba139-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba139-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba139-107">DESCRIPTION</span></span>
<span data-ttu-id="ba139-108">**A New-AzureRmVirtualNetworkSubnetConfig** parancsmag virtuális hálózati alhálózat-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ba139-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="ba139-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba139-109">EXAMPLES</span></span>

### <span data-ttu-id="ba139-110">1: virtuális hálózat létrehozása két alhálózattal és egy hálózati biztonsági csoporttal</span><span class="sxs-lookup"><span data-stu-id="ba139-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="ba139-111">Ez a példa két új alhálózat-konfigurációt hoz létre az New-AzureRmVirtualSubnetConfig parancsmag segítségével, majd virtuális hálózat létrehozására használja őket.</span><span class="sxs-lookup"><span data-stu-id="ba139-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="ba139-112">A New-AzureRmVirtualSubnetConfig sablon csak az alhálózat memória szerinti ábrázolását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ba139-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="ba139-113">Ebben a példában a frontendSubnet CIDR 10.0.1.0/24 verzióval rendelkezik, és egy hálózati biztonsági csoportra hivatkozik, amely lehetővé teszi az RDP-hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="ba139-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="ba139-114">A backendSubnet CIDR 10.0.2.0/24 verzióval rendelkezik, és ugyanarra a hálózati biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="ba139-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="ba139-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba139-115">PARAMETERS</span></span>

### <span data-ttu-id="ba139-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ba139-116">-AddressPrefix</span></span>
<span data-ttu-id="ba139-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="ba139-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba139-118">-DefaultProfile</span></span>
<span data-ttu-id="ba139-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba139-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba139-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba139-120">-Name</span></span>
<span data-ttu-id="ba139-121">A létrehozandó alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="ba139-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ba139-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ba139-123">Egy NetworkSecurityGroup-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="ba139-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ba139-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ba139-125">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="ba139-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ba139-126">-RouteTable</span></span>
<span data-ttu-id="ba139-127">Az alhálózati konfigurációhoz társított útvonal táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="ba139-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="ba139-128">-RouteTableId</span></span>
<span data-ttu-id="ba139-129">Az alhálózati konfigurációhoz társított útvonali táblázat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba139-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="ba139-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba139-130">-ServiceEndpoint</span></span>
<span data-ttu-id="ba139-131">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="ba139-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="ba139-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba139-132">CommonParameters</span></span>
<span data-ttu-id="ba139-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba139-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba139-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba139-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba139-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba139-135">INPUTS</span></span>

### <span data-ttu-id="ba139-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba139-136">None</span></span>
<span data-ttu-id="ba139-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ba139-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba139-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba139-138">OUTPUTS</span></span>

### <span data-ttu-id="ba139-139">Microsoft. Azure. commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ba139-139">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ba139-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba139-140">NOTES</span></span>

## <span data-ttu-id="ba139-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba139-141">RELATED LINKS</span></span>

[<span data-ttu-id="ba139-142">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ba139-142">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ba139-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ba139-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ba139-144">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ba139-144">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ba139-145">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ba139-145">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


