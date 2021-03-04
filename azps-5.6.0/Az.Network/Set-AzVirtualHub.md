---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: a23b2ce975a67a87a5edd58b21835e16f812055b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928561"
---
# <span data-ttu-id="13873-101">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="13873-101">Set-AzVirtualHub</span></span>

## <span data-ttu-id="13873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13873-102">SYNOPSIS</span></span>
<span data-ttu-id="13873-103">Egy virtuális központot módosítva virtuális HUb-útvonaltáblát ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="13873-103">Modifies a Virtual Hub to add a Virtual HUb Route Table to it.</span></span>

## <span data-ttu-id="13873-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13873-104">SYNTAX</span></span>

### <span data-ttu-id="13873-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13873-105">ByVirtualHubName (Default)</span></span>
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13873-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="13873-106">ByVirtualHubResourceId</span></span>
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13873-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="13873-107">ByVirtualHubObject</span></span>
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13873-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13873-108">DESCRIPTION</span></span>
<span data-ttu-id="13873-109">{{ Töltse ki a leírás }}</span><span class="sxs-lookup"><span data-stu-id="13873-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="13873-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13873-110">EXAMPLES</span></span>

### <span data-ttu-id="13873-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="13873-111">Example 1</span></span>
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

<span data-ttu-id="13873-112">Először létrehozunk egy Virtual Hub Route objektumot, és egy virtuális központi útvonaltábla-erőforrást hozunk létre vele.</span><span class="sxs-lookup"><span data-stu-id="13873-112">First we create a Virtual Hub Route object, and use it to create a Virtual Hub Route Table resource.</span></span> <span data-ttu-id="13873-113">Ezután ezt az útvonaltábla-erőforrást a virtuális központra állítva a Set-AzVirtualHub parancsot.</span><span class="sxs-lookup"><span data-stu-id="13873-113">Then we set this route table resource to the virtual hub using the Set-AzVirtualHub command.</span></span>

## <span data-ttu-id="13873-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13873-114">PARAMETERS</span></span>

### <span data-ttu-id="13873-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13873-115">-AsJob</span></span>
<span data-ttu-id="13873-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="13873-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13873-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13873-117">-DefaultProfile</span></span>
<span data-ttu-id="13873-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13873-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13873-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13873-119">-InputObject</span></span>
<span data-ttu-id="13873-120">A módosítva lévő virtuális központi objektum.</span><span class="sxs-lookup"><span data-stu-id="13873-120">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="13873-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13873-121">-Name</span></span>
<span data-ttu-id="13873-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="13873-122">The resource name.</span></span>

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

### <span data-ttu-id="13873-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13873-123">-ResourceGroupName</span></span>
<span data-ttu-id="13873-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13873-124">The resource group name.</span></span>

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

### <span data-ttu-id="13873-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13873-125">-ResourceId</span></span>
<span data-ttu-id="13873-126">A módosítani szükséges virtuális központ erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="13873-126">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="13873-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="13873-127">-RouteTable</span></span>
<span data-ttu-id="13873-128">A virtuális központhoz társított útvonaltáblák.</span><span class="sxs-lookup"><span data-stu-id="13873-128">The route tables associated with this Virtual Hub.</span></span>

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

### <span data-ttu-id="13873-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="13873-129">-Tag</span></span>
<span data-ttu-id="13873-130">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="13873-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="13873-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13873-131">-Confirm</span></span>
<span data-ttu-id="13873-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13873-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13873-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13873-133">-WhatIf</span></span>
<span data-ttu-id="13873-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13873-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13873-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13873-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13873-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13873-136">CommonParameters</span></span>
<span data-ttu-id="13873-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13873-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13873-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13873-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13873-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13873-139">INPUTS</span></span>

### <span data-ttu-id="13873-140">System.String</span><span class="sxs-lookup"><span data-stu-id="13873-140">System.String</span></span>

### <span data-ttu-id="13873-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="13873-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="13873-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13873-142">OUTPUTS</span></span>

### <span data-ttu-id="13873-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="13873-143">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="13873-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13873-144">NOTES</span></span>

## <span data-ttu-id="13873-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13873-145">RELATED LINKS</span></span>
