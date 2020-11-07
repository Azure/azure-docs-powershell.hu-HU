---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHub.md
ms.openlocfilehash: 4058f9a2ba0de1e5610773ad4af21c8bb788d58c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673153"
---
# <span data-ttu-id="29126-101">New-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="29126-101">New-AzureRmVirtualHub</span></span>

## <span data-ttu-id="29126-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29126-102">SYNOPSIS</span></span>
<span data-ttu-id="29126-103">Azure VirtualHub-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29126-103">Creates an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29126-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29126-104">SYNTAX</span></span>

### <span data-ttu-id="29126-105">ByVirtualWanObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29126-105">ByVirtualWanObject (Default)</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan>
 -AddressPrefix <String> -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29126-106">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="29126-106">ByVirtualWanResourceId</span></span>
```
New-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> -VirtualWanId <String> -AddressPrefix <String>
 -Location <String> [-HubVnetConnection <PSHubVirtualNetworkConnection[]>]
 [-RouteTable <PSVirtualHubRouteTable>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29126-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="29126-107">DESCRIPTION</span></span>
<span data-ttu-id="29126-108">Azure VirtualHub-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29126-108">Creates an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="29126-109">Példák</span><span class="sxs-lookup"><span data-stu-id="29126-109">EXAMPLES</span></span>

### <span data-ttu-id="29126-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29126-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="29126-111">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="29126-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="29126-112">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="29126-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

### <span data-ttu-id="29126-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="29126-113">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -Location "West US"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="29126-114">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="29126-114">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="29126-115">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="29126-115">The virtual hub will have the address space "10.0.1.0/24".</span></span> 

<span data-ttu-id="29126-116">Ez a példa hasonló az 1 értékhez, de egy erőforrás-azonosítóval hivatkozik a virtuális WAN-kapcsolat létrehozásához szükséges virtuális WAN-elemre.</span><span class="sxs-lookup"><span data-stu-id="29126-116">This example is similar to Example 1, but uses a resource Id to reference the Virtual WAN that is required to create the virtual Hub.</span></span>

### <span data-ttu-id="29126-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="29126-117">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="29126-118">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="29126-118">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="29126-119">A virtuális hub a következő helyet fogja tartalmazni: "10.0.1.0/24", és egy útválasztási táblázat van csatolva.</span><span class="sxs-lookup"><span data-stu-id="29126-119">The virtual hub will have the address space "10.0.1.0/24" and a route table attached.</span></span>

<span data-ttu-id="29126-120">Ez a példa hasonló a 2 példához, de egy útválasztási táblázatot is csatol a virtuális központhoz.</span><span class="sxs-lookup"><span data-stu-id="29126-120">This example is similar to Example 2, but also attaches a route table to the virtual hub.</span></span>

## <span data-ttu-id="29126-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29126-121">PARAMETERS</span></span>

### <span data-ttu-id="29126-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="29126-122">-AddressPrefix</span></span>
<span data-ttu-id="29126-123">A virtuális hub címterület-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="29126-123">The address space string for this virtual hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29126-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29126-124">-AsJob</span></span>
<span data-ttu-id="29126-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="29126-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29126-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29126-126">-DefaultProfile</span></span>
<span data-ttu-id="29126-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29126-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29126-128">-HubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="29126-128">-HubVnetConnection</span></span>
<span data-ttu-id="29126-129">A virtuális központtal társított virtuális hub-hálózati kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="29126-129">The hub virtual network connections associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="29126-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="29126-130">-Location</span></span>
<span data-ttu-id="29126-131">helyre.</span><span class="sxs-lookup"><span data-stu-id="29126-131">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29126-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="29126-132">-Name</span></span>
<span data-ttu-id="29126-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="29126-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29126-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29126-134">-ResourceGroupName</span></span>
<span data-ttu-id="29126-135">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="29126-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29126-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="29126-136">-RouteTable</span></span>
<span data-ttu-id="29126-137">A virtuális központtal társított útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="29126-137">The route table associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="29126-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="29126-138">-Tag</span></span>
<span data-ttu-id="29126-139">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="29126-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="29126-140">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="29126-140">-VirtualWan</span></span>
<span data-ttu-id="29126-141">A virtuális WAN-objektum, amelyre a hub hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="29126-141">The virtual wan object this hub is linked to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29126-142">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="29126-142">-VirtualWanId</span></span>
<span data-ttu-id="29126-143">Annak a virtuális WAN-objektumnak az azonosítója, amelyre a hub hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="29126-143">The id of virtual wan object this hub is linked to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29126-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29126-144">-Confirm</span></span>
<span data-ttu-id="29126-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29126-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29126-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29126-146">-WhatIf</span></span>
<span data-ttu-id="29126-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29126-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29126-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29126-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29126-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29126-149">CommonParameters</span></span>
<span data-ttu-id="29126-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29126-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29126-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29126-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29126-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29126-152">INPUTS</span></span>

### <span data-ttu-id="29126-153">Microsoft. Azure. commands. Network. models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="29126-153">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="29126-154">System. String</span><span class="sxs-lookup"><span data-stu-id="29126-154">System.String</span></span>

## <span data-ttu-id="29126-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29126-155">OUTPUTS</span></span>

### <span data-ttu-id="29126-156">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="29126-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="29126-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29126-157">NOTES</span></span>

## <span data-ttu-id="29126-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29126-158">RELATED LINKS</span></span>
