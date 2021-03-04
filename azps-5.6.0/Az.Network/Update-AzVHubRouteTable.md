---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVHubRouteTable.md
ms.openlocfilehash: b3b4fe711cbccd195f4549ae936fe438185c9070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918410"
---
# <span data-ttu-id="5e1b3-101">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-101">Update-AzVHubRouteTable</span></span>

## <span data-ttu-id="5e1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1b3-103">Törölje a VirtualHubbal társított központi útvonaltábla-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="5e1b3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e1b3-104">SYNTAX</span></span>

### <span data-ttu-id="5e1b3-105">ByVHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e1b3-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Update-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String>[-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1b3-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="5e1b3-106">ByVirtualHubObject</span></span>
```powershell
Update-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1b3-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="5e1b3-107">ByVHubRouteTableObject</span></span>
```powershell
Update-AzVHubRouteTable -InputObject <PSVHubRouteTable> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1b3-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="5e1b3-108">ByVHubRouteTableResourceId</span></span>
```powershell
Update-AzVHubRouteTable -ResourceId <String> [-Route <PSVHubRoute[]>] [-Label <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1b3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e1b3-109">DESCRIPTION</span></span>
<span data-ttu-id="5e1b3-110">Frissíti a megadott virtuális központhoz társított útvonaltáblát a megadott útvonalokkal vagy címkékkel.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-110">Updates the specified route table that is associated with the specified virtual hub with the provided routes or the labels.</span></span>

## <span data-ttu-id="5e1b3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e1b3-111">EXAMPLES</span></span>

### <span data-ttu-id="5e1b3-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5e1b3-112">Example 1</span></span>
```powershell
PS C:\> New-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan" -Location "westcentralus" -VirtualWANType "Standard" -AllowVnetToVnetTraffic -AllowBranchToBranchTraffic
PS C:\> $virtualWan = Get-AzVirtualWan -ResourceGroupName "testRg" -Name "testWan"

PS C:\> New-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub" -Location "westcentralus" -AddressPrefix "10.0.0.0/16" -VirtualWan $virtualWan
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName "testRg" -Name "testHub"

PS C:\> $fwIp = New-AzFirewallHubPublicIpAddress -Count 1
PS C:\> $hubIpAddresses = New-AzFirewallHubIpAddress -PublicIP $fwIp
PS C:\> New-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg" -Location "westcentralus" -Sku AZFW_Hub -VirtualHubId $virtualHub.Id -HubIPAddress $hubIpAddresses
PS C:\> $firewall = Get-AzFirewall -Name "testFirewall" -ResourceGroupName "testRg"

PS C:\> $route1 = New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> New-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route1) -Label @("testLabel")
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

PS C:\> $route2 = New-AzVHubRoute -Name "internet-traffic" -Destination @("0.0.0.0/0") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"
PS C:\> Update-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable" -Route @($route2)
PS C:\> Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "internet-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "0.0.0.0/0"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="5e1b3-113">Ez a parancs törli a virtuális központ központi útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="5e1b3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e1b3-114">PARAMETERS</span></span>

### <span data-ttu-id="5e1b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e1b3-115">-AsJob</span></span>
<span data-ttu-id="5e1b3-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5e1b3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e1b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1b3-117">-DefaultProfile</span></span>
<span data-ttu-id="5e1b3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e1b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e1b3-119">-InputObject</span></span>
<span data-ttu-id="5e1b3-120">A frissíthető vhubroutetable erőforrás.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-120">The vhubroutetable resource to Update.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-121">-Label</span><span class="sxs-lookup"><span data-stu-id="5e1b3-121">-Label</span></span>
<span data-ttu-id="5e1b3-122">A címkék listája.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-122">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5e1b3-123">-Name</span></span>
<span data-ttu-id="5e1b3-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e1b3-125">-ParentObject</span></span>
<span data-ttu-id="5e1b3-126">Az erőforrás szülő virtuális központi objektuma.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5e1b3-127">-ParentResourceName</span></span>
<span data-ttu-id="5e1b3-128">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="5e1b3-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e1b3-131">-ResourceId</span></span>
<span data-ttu-id="5e1b3-132">A frissíthető vhubroutetable erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-132">The resource id of the vhubroutetable resource to Update.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-133">-Útvonal</span><span class="sxs-lookup"><span data-stu-id="5e1b3-133">-Route</span></span>
<span data-ttu-id="5e1b3-134">Az útvonaltáblához az útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-134">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1b3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e1b3-135">-Confirm</span></span>
<span data-ttu-id="5e1b3-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1b3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1b3-137">-WhatIf</span></span>
<span data-ttu-id="5e1b3-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1b3-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1b3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1b3-140">CommonParameters</span></span>
<span data-ttu-id="5e1b3-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1b3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1b3-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e1b3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1b3-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e1b3-143">INPUTS</span></span>

### <span data-ttu-id="5e1b3-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5e1b3-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="5e1b3-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="5e1b3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5e1b3-146">System.String</span></span>

## <span data-ttu-id="5e1b3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e1b3-147">OUTPUTS</span></span>

### <span data-ttu-id="5e1b3-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-148">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="5e1b3-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e1b3-149">NOTES</span></span>

## <span data-ttu-id="5e1b3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e1b3-150">RELATED LINKS</span></span>

[<span data-ttu-id="5e1b3-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="5e1b3-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="5e1b3-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="5e1b3-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="5e1b3-154">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e1b3-154">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)