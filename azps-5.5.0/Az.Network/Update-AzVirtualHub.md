---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHub.md
ms.openlocfilehash: a07df2c6330757bf9e5b4f211429f6e2918fea39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154050"
---
# <span data-ttu-id="33b34-101">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-101">Update-AzVirtualHub</span></span>

## <span data-ttu-id="33b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33b34-102">SYNOPSIS</span></span>
<span data-ttu-id="33b34-103">Frissíti a virtuális központot.</span><span class="sxs-lookup"><span data-stu-id="33b34-103">Updates a virtual hub.</span></span>

## <span data-ttu-id="33b34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33b34-104">SYNTAX</span></span>

### <span data-ttu-id="33b34-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33b34-105">ByVirtualHubName (Default)</span></span>
```
Update-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33b34-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="33b34-106">ByVirtualHubResourceId</span></span>
```
Update-AzVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33b34-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="33b34-107">ByVirtualHubObject</span></span>
```
Update-AzVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-Sku <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33b34-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33b34-108">DESCRIPTION</span></span>
<span data-ttu-id="33b34-109">Az **Update-AzVirtualHub** parancsmag frissíti a virtuális központot.</span><span class="sxs-lookup"><span data-stu-id="33b34-109">The **Update-AzVirtualHub** cmdlet updates a virtual hub.</span></span>

## <span data-ttu-id="33b34-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33b34-110">EXAMPLES</span></span>

### <span data-ttu-id="33b34-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="33b34-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="33b34-112">A fenti egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot hoz létre az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="33b34-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="33b34-113">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="33b34-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="33b34-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="33b34-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Sku                  : Standard
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="33b34-115">A fenti egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot hoz létre az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="33b34-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="33b34-116">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="33b34-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="33b34-117">Ez a példa hasonló az 1. példához, de egy útválasztási táblát is csatol a virtuális központhoz.</span><span class="sxs-lookup"><span data-stu-id="33b34-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="33b34-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33b34-118">PARAMETERS</span></span>

### <span data-ttu-id="33b34-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="33b34-119">-AddressPrefix</span></span>
<span data-ttu-id="33b34-120">A virtuális központ címterület-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="33b34-120">The address space string for this virtual hub.</span></span>

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

### <span data-ttu-id="33b34-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33b34-121">-AsJob</span></span>
<span data-ttu-id="33b34-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="33b34-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33b34-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b34-123">-DefaultProfile</span></span>
<span data-ttu-id="33b34-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33b34-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b34-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="33b34-125">-HubVnetConnection</span></span>
<span data-ttu-id="33b34-126">A virtuális központhoz társított központi virtuális hálózati kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="33b34-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="33b34-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33b34-127">-InputObject</span></span>
<span data-ttu-id="33b34-128">A módosítva lévő virtuális központi objektum.</span><span class="sxs-lookup"><span data-stu-id="33b34-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33b34-129">-Name</span><span class="sxs-lookup"><span data-stu-id="33b34-129">-Name</span></span>
<span data-ttu-id="33b34-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="33b34-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b34-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b34-131">-ResourceGroupName</span></span>
<span data-ttu-id="33b34-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33b34-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b34-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33b34-133">-ResourceId</span></span>
<span data-ttu-id="33b34-134">A módosítható virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33b34-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b34-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="33b34-135">-RouteTable</span></span>
<span data-ttu-id="33b34-136">A virtuális központhoz társított útvonaltábla.</span><span class="sxs-lookup"><span data-stu-id="33b34-136">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="33b34-137">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="33b34-137">-Sku</span></span>
<span data-ttu-id="33b34-138">A virtuális központ termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="33b34-138">The sku of the Virtual Hub.</span></span>

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

### <span data-ttu-id="33b34-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="33b34-139">-Tag</span></span>
<span data-ttu-id="33b34-140">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="33b34-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="33b34-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33b34-141">-Confirm</span></span>
<span data-ttu-id="33b34-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33b34-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b34-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b34-143">-WhatIf</span></span>
<span data-ttu-id="33b34-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="33b34-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33b34-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33b34-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b34-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b34-146">CommonParameters</span></span>
<span data-ttu-id="33b34-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b34-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b34-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33b34-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b34-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33b34-149">INPUTS</span></span>

### <span data-ttu-id="33b34-150">System.String</span><span class="sxs-lookup"><span data-stu-id="33b34-150">System.String</span></span>

### <span data-ttu-id="33b34-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="33b34-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33b34-152">OUTPUTS</span></span>

### <span data-ttu-id="33b34-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="33b34-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33b34-154">NOTES</span></span>

## <span data-ttu-id="33b34-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33b34-155">RELATED LINKS</span></span>

[<span data-ttu-id="33b34-156">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-156">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="33b34-157">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-157">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="33b34-158">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="33b34-158">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)
