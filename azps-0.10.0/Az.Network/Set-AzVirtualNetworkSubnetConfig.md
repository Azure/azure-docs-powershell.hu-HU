---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 73649f0f04cf1de07d991cb454b44308c4ff6443
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843550"
---
# <span data-ttu-id="9e001-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e001-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9e001-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e001-102">SYNOPSIS</span></span>
<span data-ttu-id="9e001-103">Egy virtuális hálózat alhálózat-konfigurációjának cél állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

## <span data-ttu-id="9e001-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e001-104">SYNTAX</span></span>

### <span data-ttu-id="9e001-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9e001-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e001-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e001-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e001-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e001-107">DESCRIPTION</span></span>
<span data-ttu-id="9e001-108">A **set-AzVirtualNetworkSubnetConfig** parancsmag a cél állapotát az Azure virtuális hálózatban lévő alhálózati konfigurációhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="9e001-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="9e001-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9e001-109">EXAMPLES</span></span>

### <span data-ttu-id="9e001-110">1: az alhálózat cím előtagjának módosítása</span><span class="sxs-lookup"><span data-stu-id="9e001-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9e001-111">Ez a példa egy virtuális hálózatot hoz létre egy alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="9e001-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="9e001-112">Ezután a hívások Set-AzVirtualNetworkSubnetConfig az alhálózat AddressPrefix módosítására.</span><span class="sxs-lookup"><span data-stu-id="9e001-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="9e001-113">Ez a funkció csak a virtuális hálózat memóriában való megjelenítését befolyásolja.</span><span class="sxs-lookup"><span data-stu-id="9e001-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9e001-114">Ezt követően a rendszer az Azure virtuális hálózatának módosítását kéri Set-AzVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9e001-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="9e001-115">2: hálózati biztonsági csoport hozzáadása alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="9e001-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="9e001-116">Ez a példa olyan erőforráscsoportot hoz létre, amelynek egyetlen virtuális hálózata csak egy alhálózatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9e001-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="9e001-117">Ekkor létrehoz egy hálózati biztonsági csoportot az RDP-forgalom engedélyezési szabályával.</span><span class="sxs-lookup"><span data-stu-id="9e001-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="9e001-118">A Set-AzVirtualNetworkSubnetConfig parancsmag a felületi alhálózat memóriában való megjelenítésének módosítására szolgál, hogy az az újonnan létrehozott hálózati biztonsági csoportra mutasson.</span><span class="sxs-lookup"><span data-stu-id="9e001-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="9e001-119">Ezt követően az Set-AzVirtualNetwork parancsmag a módosított állapotnak a szolgáltatásba való visszaírását kéri.</span><span class="sxs-lookup"><span data-stu-id="9e001-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="9e001-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e001-120">PARAMETERS</span></span>

### <span data-ttu-id="9e001-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9e001-121">-AddressPrefix</span></span>
<span data-ttu-id="9e001-122">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="9e001-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e001-123">-DefaultProfile</span></span>
<span data-ttu-id="9e001-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e001-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e001-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e001-125">-Name</span></span>
<span data-ttu-id="9e001-126">A parancsmag által konfigurált alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="9e001-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e001-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9e001-128">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="9e001-129">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9e001-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="9e001-130">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="9e001-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9e001-131">-RouteTable</span></span>
<span data-ttu-id="9e001-132">A hálózati biztonsági csoporthoz tartozó Route Table objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9e001-133">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="9e001-133">-RouteTableId</span></span>
<span data-ttu-id="9e001-134">Annak az útválasztási objektumnak az AZONOSÍTÓját adja meg, amely a hálózat biztonsági csoportjához van társítva.</span><span class="sxs-lookup"><span data-stu-id="9e001-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9e001-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e001-135">-ServiceEndpoint</span></span>
<span data-ttu-id="9e001-136">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="9e001-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="9e001-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e001-137">-VirtualNetwork</span></span>
<span data-ttu-id="9e001-138">Az alhálózati konfigurációt tartalmazó **VirtualNetwork** -objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e001-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="9e001-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e001-139">CommonParameters</span></span>
<span data-ttu-id="9e001-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e001-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e001-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e001-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e001-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e001-142">INPUTS</span></span>

### <span data-ttu-id="9e001-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e001-143">PSVirtualNetwork</span></span>
<span data-ttu-id="9e001-144">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9e001-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="9e001-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e001-145">OUTPUTS</span></span>

### <span data-ttu-id="9e001-146">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e001-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9e001-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e001-147">NOTES</span></span>

## <span data-ttu-id="9e001-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e001-148">RELATED LINKS</span></span>

[<span data-ttu-id="9e001-149">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e001-149">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e001-150">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e001-150">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e001-151">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e001-151">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9e001-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9e001-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)


