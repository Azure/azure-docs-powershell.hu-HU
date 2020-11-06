---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualHub.md
ms.openlocfilehash: 188d449e47155739b4bc532c12b0e9193781c7c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498259"
---
# <span data-ttu-id="36e82-101">Update-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36e82-101">Update-AzureRmVirtualHub</span></span>

## <span data-ttu-id="36e82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36e82-102">SYNOPSIS</span></span>
<span data-ttu-id="36e82-103">Egy virtuális központot frissít egy szándékolt cél állapotba.</span><span class="sxs-lookup"><span data-stu-id="36e82-103">Updates a Virtual Hub to an intended goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36e82-104">SYNTAX</span></span>

### <span data-ttu-id="36e82-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36e82-105">ByVirtualHubName (Default)</span></span>
```
Update-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36e82-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="36e82-106">ByVirtualHubResourceId</span></span>
```
Update-AzureRmVirtualHub -ResourceId <String> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36e82-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="36e82-107">ByVirtualHubObject</span></span>
```
Update-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AddressPrefix <String>]
 [-HubVnetConnection <PSHubVirtualNetworkConnection[]>] [-RouteTable <PSVirtualHubRouteTable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36e82-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="36e82-108">DESCRIPTION</span></span>
<span data-ttu-id="36e82-109">Egy virtuális központot frissít egy szándékolt cél állapotba.</span><span class="sxs-lookup"><span data-stu-id="36e82-109">Updates a Virtual Hub to an intended goal state.</span></span>

## <span data-ttu-id="36e82-110">Példák</span><span class="sxs-lookup"><span data-stu-id="36e82-110">EXAMPLES</span></span>

### <span data-ttu-id="36e82-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36e82-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Update-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.2.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.2.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36e82-112">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="36e82-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36e82-113">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="36e82-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="36e82-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="36e82-114">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> Update-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 192.168.2.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="36e82-115">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="36e82-115">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="36e82-116">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="36e82-116">The virtual hub will have the address space "10.0.1.0/24".</span></span>
<span data-ttu-id="36e82-117">Ez a példa hasonló az 1 értékhez, de egy útválasztási táblázatot is csatol a virtuális központhoz.</span><span class="sxs-lookup"><span data-stu-id="36e82-117">This example is similar to Example 1, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="36e82-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36e82-118">PARAMETERS</span></span>

### <span data-ttu-id="36e82-119">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="36e82-119">-AddressPrefix</span></span>
<span data-ttu-id="36e82-120">A virtuális hub címterület-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="36e82-120">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36e82-121">-AsJob</span></span>
<span data-ttu-id="36e82-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36e82-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e82-123">-DefaultProfile</span></span>
<span data-ttu-id="36e82-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36e82-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-125">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="36e82-125">-HubVnetConnection</span></span>
<span data-ttu-id="36e82-126">A virtuális központtal társított virtuális hub-hálózati kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="36e82-126">The hub virtual network connections associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e82-127">-InputObject</span></span>
<span data-ttu-id="36e82-128">A módosítani kívánt virtuális hub-objektum.</span><span class="sxs-lookup"><span data-stu-id="36e82-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36e82-129">-Name</span></span>
<span data-ttu-id="36e82-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="36e82-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e82-131">-ResourceGroupName</span></span>
<span data-ttu-id="36e82-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="36e82-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e82-133">-ResourceId</span></span>
<span data-ttu-id="36e82-134">A módosítani kívánt virtuális hub erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="36e82-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="36e82-135">-RouteTable</span></span>
<span data-ttu-id="36e82-136">A virtuális központtal társított útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="36e82-136">The route table associated with this Virtual Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="36e82-137">-Tag</span></span>
<span data-ttu-id="36e82-138">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="36e82-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36e82-139">-Confirm</span></span>
<span data-ttu-id="36e82-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36e82-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e82-141">-WhatIf</span></span>
<span data-ttu-id="36e82-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36e82-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e82-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36e82-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e82-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e82-144">CommonParameters</span></span>
<span data-ttu-id="36e82-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36e82-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e82-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e82-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e82-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e82-147">INPUTS</span></span>

### <span data-ttu-id="36e82-148">System. String</span><span class="sxs-lookup"><span data-stu-id="36e82-148">System.String</span></span>

### <span data-ttu-id="36e82-149">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36e82-149">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36e82-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e82-150">OUTPUTS</span></span>

### <span data-ttu-id="36e82-151">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="36e82-151">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="36e82-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36e82-152">NOTES</span></span>

## <span data-ttu-id="36e82-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36e82-153">RELATED LINKS</span></span>
