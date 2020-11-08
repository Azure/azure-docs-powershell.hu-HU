---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194243"
---
# <span data-ttu-id="cf684-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cf684-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="cf684-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf684-102">SYNOPSIS</span></span>
<span data-ttu-id="cf684-103">Azure VirtualHub-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf684-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="cf684-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf684-104">SYNTAX</span></span>

### <span data-ttu-id="cf684-105">ByVirtualWanObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf684-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf684-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cf684-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf684-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf684-107">DESCRIPTION</span></span>
<span data-ttu-id="cf684-108">Azure VirtualHub-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf684-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="cf684-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf684-109">EXAMPLES</span></span>

### <span data-ttu-id="cf684-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf684-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="cf684-111">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="cf684-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="cf684-112">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="cf684-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="cf684-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf684-113">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="cf684-114">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="cf684-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="cf684-115">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="cf684-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="cf684-116">Ez a példa hasonló az 1 értékhez, de egy erőforrás-azonosítóval hivatkozik a virtuális WAN-kapcsolat létrehozásához szükséges virtuális WAN-elemre.</span><span class="sxs-lookup"><span data-stu-id="cf684-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="cf684-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="cf684-117">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
RouteTables                           : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="cf684-118">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="cf684-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="cf684-119">A virtuális hub a következő helyet fogja tartalmazni: "10.0.1.0/24", és egy útválasztási táblázat van csatolva.</span><span class="sxs-lookup"><span data-stu-id="cf684-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="cf684-120">Ez a példa hasonló a 2 példához, de egy útválasztási táblázatot is csatol a virtuális központhoz.</span><span class="sxs-lookup"><span data-stu-id="cf684-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="cf684-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf684-121">PARAMETERS</span></span>

### <span data-ttu-id="cf684-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cf684-122">-AddressPrefix</span></span>
<span data-ttu-id="cf684-123">A virtuális hub címterület-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="cf684-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="cf684-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf684-124">-AsJob</span></span>
<span data-ttu-id="cf684-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cf684-125">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf684-126">-DefaultProfile</span></span>
<span data-ttu-id="cf684-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf684-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf684-128">-HubVnetConnection</span></span>
<span data-ttu-id="cf684-129">A virtuális központtal társított virtuális hub-hálózati kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="cf684-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cf684-130">-Location</span></span>
<span data-ttu-id="cf684-131">helyre.</span><span class="sxs-lookup"><span data-stu-id="cf684-131">location.</span></span>

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

### <span data-ttu-id="cf684-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf684-132">-Name</span></span>
<span data-ttu-id="cf684-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cf684-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf684-134">-ResourceGroupName</span></span>
<span data-ttu-id="cf684-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cf684-135">The resource group name.</span></span>

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

### <span data-ttu-id="cf684-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="cf684-136">-RouteTable</span></span>
<span data-ttu-id="cf684-137">A virtuális központtal társított útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="cf684-137">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf684-138">-Sku</span></span>
<span data-ttu-id="cf684-139">A virtuális hub SKU-je.</span><span class="sxs-lookup"><span data-stu-id="cf684-139">The sku of the Virtual Hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="cf684-140">-Tag</span></span>
<span data-ttu-id="cf684-141">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cf684-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="cf684-142">-VirtualWan</span></span>
<span data-ttu-id="cf684-143">A virtuális WAN-objektum, amelyre a hub hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="cf684-143">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="cf684-144">-VirtualWanId</span></span>
<span data-ttu-id="cf684-145">Annak a virtuális WAN-objektumnak az azonosítója, amelyre a hub hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="cf684-145">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf684-146">-Confirm</span></span>
<span data-ttu-id="cf684-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf684-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf684-148">-WhatIf</span></span>
<span data-ttu-id="cf684-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf684-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf684-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf684-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf684-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf684-151">CommonParameters</span></span>
<span data-ttu-id="cf684-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf684-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf684-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf684-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf684-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf684-154">INPUTS</span></span>

### <span data-ttu-id="cf684-155">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cf684-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="cf684-156">System. String</span><span class="sxs-lookup"><span data-stu-id="cf684-156">System.String</span></span>

## <span data-ttu-id="cf684-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf684-157">OUTPUTS</span></span>

### <span data-ttu-id="cf684-158">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cf684-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="cf684-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf684-159">NOTES</span></span>

## <span data-ttu-id="cf684-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf684-160">RELATED LINKS</span></span>

[<span data-ttu-id="cf684-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cf684-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="cf684-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cf684-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="cf684-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cf684-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)