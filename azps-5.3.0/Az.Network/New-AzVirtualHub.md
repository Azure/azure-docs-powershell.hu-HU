---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHub.md
ms.openlocfilehash: d005ef841828dc1fe37915c4a7b0d28ad93e3b44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467324"
---
# <span data-ttu-id="e12ab-101">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e12ab-101">New-AzVirtualHub</span></span>

## <span data-ttu-id="e12ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e12ab-103">Létrehoz egy Azure VirtualHub-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e12ab-103">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e12ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e12ab-104">SYNTAX</span></span>

### <span data-ttu-id="e12ab-105">ByVirtualWanObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e12ab-105">ByVirtualWanObject (Default)</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ab-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e12ab-106">ByVirtualWanResourceId</span></span>
```
New-AzVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable[]>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e12ab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e12ab-107">DESCRIPTION</span></span>
<span data-ttu-id="e12ab-108">Létrehoz egy Azure VirtualHub-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e12ab-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e12ab-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e12ab-109">EXAMPLES</span></span>

### <span data-ttu-id="e12ab-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="e12ab-110">Example 1</span></span>

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

<span data-ttu-id="e12ab-111">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e12ab-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e12ab-112">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="e12ab-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="e12ab-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e12ab-113">Example 2</span></span>

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

<span data-ttu-id="e12ab-114">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e12ab-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e12ab-115">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="e12ab-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="e12ab-116">Ez a példa hasonló az 1. példához, de egy erőforrás-azonosítót használva hivatkozik a virtuális WAN-re, amely a virtuális központ létrehozásához szükséges.</span><span class="sxs-lookup"><span data-stu-id="e12ab-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="e12ab-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="e12ab-117">Example 3</span></span>

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

<span data-ttu-id="e12ab-118">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="e12ab-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e12ab-119">A virtuális központ a "10.0.1.0/24" címterületet és egy útválasztási táblát fog csatolni.</span><span class="sxs-lookup"><span data-stu-id="e12ab-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="e12ab-120">Ez a példa hasonló a 2. példához, de egy útválasztási táblát is csatol a virtuális központhoz.</span><span class="sxs-lookup"><span data-stu-id="e12ab-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="e12ab-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12ab-121">PARAMETERS</span></span>

### <span data-ttu-id="e12ab-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e12ab-122">-AddressPrefix</span></span>
<span data-ttu-id="e12ab-123">A virtuális központ címterület-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="e12ab-123">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="e12ab-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e12ab-124">-AsJob</span></span>
<span data-ttu-id="e12ab-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e12ab-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e12ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12ab-126">-DefaultProfile</span></span>
<span data-ttu-id="e12ab-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e12ab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e12ab-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e12ab-128">-HubVnetConnection</span></span>
<span data-ttu-id="e12ab-129">A virtuális központhoz társított központi virtuális hálózati kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="e12ab-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e12ab-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e12ab-130">-Location</span></span>
<span data-ttu-id="e12ab-131">helyére.</span><span class="sxs-lookup"><span data-stu-id="e12ab-131">location.</span></span>

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

### <span data-ttu-id="e12ab-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e12ab-132">-Name</span></span>
<span data-ttu-id="e12ab-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e12ab-133">The resource name.</span></span>

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

### <span data-ttu-id="e12ab-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12ab-134">-ResourceGroupName</span></span>
<span data-ttu-id="e12ab-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e12ab-135">The resource group name.</span></span>

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

### <span data-ttu-id="e12ab-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e12ab-136">-RouteTable</span></span>
<span data-ttu-id="e12ab-137">A virtuális központhoz társított útvonaltábla.</span><span class="sxs-lookup"><span data-stu-id="e12ab-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="e12ab-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="e12ab-138">-Sku</span></span>
<span data-ttu-id="e12ab-139">A virtuális központ termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="e12ab-139">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="e12ab-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="e12ab-140">-Tag</span></span>
<span data-ttu-id="e12ab-141">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="e12ab-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e12ab-142">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e12ab-142">-VirtualWan</span></span>
<span data-ttu-id="e12ab-143">A virtuális wan objektum, amelyhez a központ kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="e12ab-143">The virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="e12ab-144">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="e12ab-144">-VirtualWanId</span></span>
<span data-ttu-id="e12ab-145">Annak a virtuális wan objektumnak az azonosítója, amelyhez a központ kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="e12ab-145">The id of virtual wan object this hub is linked to.</span></span>

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

### <span data-ttu-id="e12ab-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e12ab-146">-Confirm</span></span>
<span data-ttu-id="e12ab-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e12ab-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12ab-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12ab-148">-WhatIf</span></span>
<span data-ttu-id="e12ab-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e12ab-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12ab-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e12ab-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12ab-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12ab-151">CommonParameters</span></span>
<span data-ttu-id="e12ab-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12ab-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12ab-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e12ab-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12ab-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e12ab-154">INPUTS</span></span>

### <span data-ttu-id="e12ab-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e12ab-155">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="e12ab-156">System.String</span><span class="sxs-lookup"><span data-stu-id="e12ab-156">System.String</span></span>

## <span data-ttu-id="e12ab-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e12ab-157">OUTPUTS</span></span>

### <span data-ttu-id="e12ab-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e12ab-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e12ab-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e12ab-159">NOTES</span></span>

## <span data-ttu-id="e12ab-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e12ab-160">RELATED LINKS</span></span>

[<span data-ttu-id="e12ab-161">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e12ab-161">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e12ab-162">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e12ab-162">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="e12ab-163">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e12ab-163">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
