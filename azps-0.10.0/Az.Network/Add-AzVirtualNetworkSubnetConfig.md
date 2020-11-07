---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 01116d3a2ad2636776fe29a0e36e34568624f2c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841786"
---
# <span data-ttu-id="722ef-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="722ef-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="722ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="722ef-102">SYNOPSIS</span></span>
<span data-ttu-id="722ef-103">Alhálózat-konfiguráció felvétele virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="722ef-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="722ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="722ef-104">SYNTAX</span></span>

### <span data-ttu-id="722ef-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="722ef-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="722ef-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="722ef-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="722ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="722ef-107">DESCRIPTION</span></span>
<span data-ttu-id="722ef-108">Az **Add-AzVirtualNetworkSubnetConfig** parancsmag alhálózat-konfigurációt ad egy meglévő Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="722ef-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="722ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="722ef-109">EXAMPLES</span></span>

### <span data-ttu-id="722ef-110">1: alhálózat felvétele meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="722ef-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="722ef-111">Ez a példa először létrehoz egy erőforráscsoportot a létrehozandó erőforrások tárolójából.</span><span class="sxs-lookup"><span data-stu-id="722ef-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="722ef-112">Ekkor létrehoz egy alhálózat-konfigurációt, és a virtuális hálózat létrehozásához használja azt.</span><span class="sxs-lookup"><span data-stu-id="722ef-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="722ef-113">A rendszer ezután felveszi az Add-AzVirtualNetworkSubnetConfig a virtuális hálózat memóriában való megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="722ef-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="722ef-114">A Set-AzVirtualNetwork parancs frissíti a meglévő virtuális hálózatot az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="722ef-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="722ef-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="722ef-115">PARAMETERS</span></span>

### <span data-ttu-id="722ef-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="722ef-116">-AddressPrefix</span></span>
<span data-ttu-id="722ef-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="722ef-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="722ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722ef-118">-DefaultProfile</span></span>
<span data-ttu-id="722ef-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="722ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="722ef-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="722ef-120">-Name</span></span>
<span data-ttu-id="722ef-121">A hozzáadni kívánt alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="722ef-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="722ef-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="722ef-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="722ef-123">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="722ef-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="722ef-124">Ez a parancsmag a virtuális hálózati alhálózat-konfigurációt hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="722ef-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="722ef-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="722ef-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="722ef-126">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="722ef-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="722ef-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="722ef-127">-RouteTable</span></span>
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

### <span data-ttu-id="722ef-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="722ef-128">-RouteTableId</span></span>
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

### <span data-ttu-id="722ef-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="722ef-129">-ServiceEndpoint</span></span>
<span data-ttu-id="722ef-130">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="722ef-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="722ef-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="722ef-131">-VirtualNetwork</span></span>
<span data-ttu-id="722ef-132">Azt a **VirtualNetwork** -objektumot adja meg, amelybe alhálózat-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="722ef-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="722ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722ef-133">CommonParameters</span></span>
<span data-ttu-id="722ef-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="722ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722ef-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722ef-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722ef-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="722ef-136">INPUTS</span></span>

### <span data-ttu-id="722ef-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="722ef-137">PSVirtualNetwork</span></span>
<span data-ttu-id="722ef-138">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="722ef-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="722ef-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="722ef-139">OUTPUTS</span></span>

### <span data-ttu-id="722ef-140">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="722ef-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="722ef-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="722ef-141">NOTES</span></span>

## <span data-ttu-id="722ef-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="722ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="722ef-143">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="722ef-143">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="722ef-144">Új – AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="722ef-144">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="722ef-145">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="722ef-145">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="722ef-146">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="722ef-146">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


