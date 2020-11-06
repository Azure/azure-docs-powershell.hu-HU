---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: eb684d6b51cdbe6d640b8bb91e2bfdd9b5f8c0b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501495"
---
# <span data-ttu-id="9b902-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b902-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9b902-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b902-102">SYNOPSIS</span></span>
<span data-ttu-id="9b902-103">Egy virtuális hálózat alhálózat-konfigurációjának cél állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b902-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b902-104">SYNTAX</span></span>

### <span data-ttu-id="9b902-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b902-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b902-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b902-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b902-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b902-107">DESCRIPTION</span></span>
<span data-ttu-id="9b902-108">A **set-AzureRmVirtualNetworkSubnetConfig** parancsmag a cél állapotát az Azure virtuális hálózatban lévő alhálózati konfigurációhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="9b902-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="9b902-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9b902-109">EXAMPLES</span></span>

### <span data-ttu-id="9b902-110">1: az alhálózat cím előtagjának módosítása</span><span class="sxs-lookup"><span data-stu-id="9b902-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="9b902-111">Ez a példa egy virtuális hálózatot hoz létre egy alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="9b902-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="9b902-112">Ezután a hívások Set-AzureRmVirtualNetworkSubnetConfig az alhálózat AddressPrefix módosítására.</span><span class="sxs-lookup"><span data-stu-id="9b902-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="9b902-113">Ez a funkció csak a virtuális hálózat memóriában való megjelenítését befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="9b902-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9b902-114">Ezt követően a rendszer az Azure virtuális hálózatának módosítását kéri Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9b902-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="9b902-115">2: hálózati biztonsági csoport hozzáadása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="9b902-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="9b902-116">Ez a példa olyan erőforráscsoportot hoz létre, amelynek egyetlen virtuális hálózata csak egy alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9b902-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="9b902-117">Ekkor létrehoz egy hálózati biztonsági csoportot az RDP-forgalom engedélyezési szabályával.</span><span class="sxs-lookup"><span data-stu-id="9b902-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="9b902-118">A Set-AzureRmVirtualNetworkSubnetConfig parancsmag a felületi alhálózat memóriában való megjelenítésének módosítására szolgál, hogy az az újonnan létrehozott hálózati biztonsági csoportra mutasson.</span><span class="sxs-lookup"><span data-stu-id="9b902-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="9b902-119">Ezt követően az Set-AzureRmVirtualNetwork parancsmag a módosított állapotnak a szolgáltatásba való visszaírását kéri.</span><span class="sxs-lookup"><span data-stu-id="9b902-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="9b902-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b902-120">PARAMETERS</span></span>

### <span data-ttu-id="9b902-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9b902-121">-AddressPrefix</span></span>
<span data-ttu-id="9b902-122">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="9b902-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b902-123">-DefaultProfile</span></span>
<span data-ttu-id="9b902-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b902-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b902-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b902-125">-Name</span></span>
<span data-ttu-id="9b902-126">A parancsmag által konfigurált alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="9b902-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b902-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9b902-128">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="9b902-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9b902-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="9b902-130">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="9b902-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9b902-131">-RouteTable</span></span>
<span data-ttu-id="9b902-132">A hálózati biztonsági csoporthoz tartozó Route Table objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9b902-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="9b902-133">-RouteTableId</span></span>
<span data-ttu-id="9b902-134">Annak az útválasztási objektumnak az AZONOSÍTÓját adja meg, amely a hálózat biztonsági csoportjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="9b902-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9b902-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b902-135">-ServiceEndpoint</span></span>
<span data-ttu-id="9b902-136">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="9b902-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="9b902-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9b902-137">-VirtualNetwork</span></span>
<span data-ttu-id="9b902-138">Az alhálózati konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b902-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b902-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b902-139">CommonParameters</span></span>
<span data-ttu-id="9b902-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b902-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b902-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b902-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b902-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b902-142">INPUTS</span></span>

### <span data-ttu-id="9b902-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9b902-143">PSVirtualNetwork</span></span>
<span data-ttu-id="9b902-144">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9b902-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="9b902-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b902-145">OUTPUTS</span></span>

### <span data-ttu-id="9b902-146">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9b902-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9b902-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b902-147">NOTES</span></span>

## <span data-ttu-id="9b902-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b902-148">RELATED LINKS</span></span>

[<span data-ttu-id="9b902-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b902-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9b902-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b902-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9b902-151">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b902-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9b902-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9b902-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


