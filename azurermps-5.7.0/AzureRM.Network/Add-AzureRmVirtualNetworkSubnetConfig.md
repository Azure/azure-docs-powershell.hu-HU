---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 0987823d2658778266f861a5115962d6cf8c4830
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499787"
---
# <span data-ttu-id="8fd13-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8fd13-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="8fd13-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fd13-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd13-103">Alhálózat-konfiguráció felvétele virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="8fd13-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd13-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fd13-104">SYNTAX</span></span>

### <span data-ttu-id="8fd13-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fd13-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fd13-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fd13-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd13-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fd13-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd13-108">Az **Add-AzureRmVirtualNetworkSubnetConfig** parancsmag alhálózat-konfigurációt ad egy meglévő Azure virtuális hálózathoz.</span><span class="sxs-lookup"><span data-stu-id="8fd13-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="8fd13-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8fd13-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd13-110">1: alhálózat felvétele meglévő virtuális hálózatba</span><span class="sxs-lookup"><span data-stu-id="8fd13-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="8fd13-111">Ez a példa először létrehoz egy erőforráscsoportot a létrehozandó erőforrások tárolójából.</span><span class="sxs-lookup"><span data-stu-id="8fd13-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="8fd13-112">Ekkor létrehoz egy alhálózat-konfigurációt, és a virtuális hálózat létrehozásához használja azt.</span><span class="sxs-lookup"><span data-stu-id="8fd13-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="8fd13-113">A rendszer ezután felveszi az Add-AzureRmVirtualNetworkSubnetConfig a virtuális hálózat memóriában való megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8fd13-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="8fd13-114">A Set-AzureRmVirtualNetwork parancs frissíti a meglévő virtuális hálózatot az új alhálózattal.</span><span class="sxs-lookup"><span data-stu-id="8fd13-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="8fd13-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fd13-115">PARAMETERS</span></span>

### <span data-ttu-id="8fd13-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8fd13-116">-AddressPrefix</span></span>
<span data-ttu-id="8fd13-117">Az alhálózati konfiguráció IP-címeinek tartományát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fd13-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="8fd13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd13-118">-DefaultProfile</span></span>
<span data-ttu-id="8fd13-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fd13-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd13-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fd13-120">-Name</span></span>
<span data-ttu-id="8fd13-121">A hozzáadni kívánt alhálózat-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fd13-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="8fd13-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fd13-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8fd13-123">Egy **NetworkSecurityGroup** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8fd13-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="8fd13-124">Ez a parancsmag a virtuális hálózati alhálózat-konfigurációt hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="8fd13-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fd13-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8fd13-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8fd13-126">Egy hálózati biztonsági csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fd13-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="8fd13-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8fd13-127">-RouteTable</span></span>
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

### <span data-ttu-id="8fd13-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="8fd13-128">-RouteTableId</span></span>
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

### <span data-ttu-id="8fd13-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fd13-129">-ServiceEndpoint</span></span>
<span data-ttu-id="8fd13-130">A szolgáltatás végpontjának értéke</span><span class="sxs-lookup"><span data-stu-id="8fd13-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="8fd13-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8fd13-131">-VirtualNetwork</span></span>
<span data-ttu-id="8fd13-132">Azt a **VirtualNetwork** -objektumot adja meg, amelybe alhálózat-konfigurációt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="8fd13-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="8fd13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd13-133">CommonParameters</span></span>
<span data-ttu-id="8fd13-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fd13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd13-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd13-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd13-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd13-136">INPUTS</span></span>

### <span data-ttu-id="8fd13-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8fd13-137">PSVirtualNetwork</span></span>
<span data-ttu-id="8fd13-138">A ' VirtualNetwork ' paraméter az "PSVirtualNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8fd13-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="8fd13-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd13-139">OUTPUTS</span></span>

### <span data-ttu-id="8fd13-140">Microsoft. Azure. commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8fd13-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8fd13-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fd13-141">NOTES</span></span>

## <span data-ttu-id="8fd13-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fd13-142">RELATED LINKS</span></span>

[<span data-ttu-id="8fd13-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8fd13-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8fd13-144">Új – AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8fd13-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8fd13-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8fd13-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8fd13-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8fd13-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


