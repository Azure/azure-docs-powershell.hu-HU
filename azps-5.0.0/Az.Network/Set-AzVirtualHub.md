---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194214"
---
# <span data-ttu-id="a85c8-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a85c8-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="a85c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a85c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a85c8-103">Módosítja a virtuális hubot a virtuális HUb-útválasztási táblázat hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="a85c8-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="a85c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a85c8-104">SYNTAX</span></span>

### <span data-ttu-id="a85c8-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a85c8-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a85c8-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a85c8-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a85c8-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a85c8-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85c8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a85c8-108">DESCRIPTION</span></span>
<span data-ttu-id="a85c8-109">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="a85c8-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="a85c8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a85c8-110">EXAMPLES</span></span>

### <span data-ttu-id="a85c8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a85c8-111">Example 1</span></span>
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

<span data-ttu-id="a85c8-112">Először hozzunk létre egy virtuális hub Route-objektumot, és a virtuális hub Route Table-erőforrás létrehozásához használjuk azt.</span><span class="sxs-lookup"><span data-stu-id="a85c8-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="a85c8-113">Ezután az útválasztási táblázat erőforrását a virtuális központba a Set-AzVirtualHub parancs segítségével állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="a85c8-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="a85c8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a85c8-114">PARAMETERS</span></span>

### <span data-ttu-id="a85c8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a85c8-115">-AsJob</span></span>
<span data-ttu-id="a85c8-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a85c8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a85c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85c8-117">-DefaultProfile</span></span>
<span data-ttu-id="a85c8-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a85c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a85c8-119">-InputObject</span></span>
<span data-ttu-id="a85c8-120">A módosítani kívánt virtuális hub-objektum.</span><span class="sxs-lookup"><span data-stu-id="a85c8-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="a85c8-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a85c8-121">-Name</span></span>
<span data-ttu-id="a85c8-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a85c8-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="a85c8-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a85c8-124">The resource group name.</span></span>

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

### <span data-ttu-id="a85c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a85c8-125">-ResourceId</span></span>
<span data-ttu-id="a85c8-126">A módosítani kívánt virtuális hub erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a85c8-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="a85c8-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a85c8-127">-RouteTable</span></span>
<span data-ttu-id="a85c8-128">A virtuális hubhoz társított útválasztási táblák.</span><span class="sxs-lookup"><span data-stu-id="a85c8-128">The route tables associated with this Virtual Hub.</span></span>

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85c8-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="a85c8-129">-Tag</span></span>
<span data-ttu-id="a85c8-130">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="a85c8-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a85c8-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a85c8-131">-Confirm</span></span>
<span data-ttu-id="a85c8-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a85c8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85c8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85c8-133">-WhatIf</span></span>
<span data-ttu-id="a85c8-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a85c8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85c8-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a85c8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85c8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85c8-136">CommonParameters</span></span>
<span data-ttu-id="a85c8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a85c8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85c8-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a85c8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85c8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85c8-139">INPUTS</span></span>

### <span data-ttu-id="a85c8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a85c8-140">System.String</span></span>

### <span data-ttu-id="a85c8-141">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a85c8-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a85c8-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a85c8-142">OUTPUTS</span></span>

### <span data-ttu-id="a85c8-143">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a85c8-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="a85c8-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a85c8-144">NOTES</span></span>

## <span data-ttu-id="a85c8-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a85c8-145">RELATED LINKS</span></span>