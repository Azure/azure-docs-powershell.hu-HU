---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRouteTable.md
ms.openlocfilehash: d9c7b4895d05b4f55ef91705062db7c200d702cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330605"
---
# <span data-ttu-id="f7879-101">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-101">New-AzVHubRouteTable</span></span>

## <span data-ttu-id="f7879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7879-102">SYNOPSIS</span></span>
<span data-ttu-id="f7879-103">Egy VirtualHubbal társított központi útvonaltábla-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f7879-103">Creates a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="f7879-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7879-104">SYNTAX</span></span>

### <span data-ttu-id="f7879-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7879-105">ByVirtualHubName (Default)</span></span>

```powershell
New-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7879-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f7879-106">ByVirtualHubObject</span></span>

```powershell
New-AzVHubRouteTable -Name <String> -ParentObject <PSVirtualHub> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7879-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f7879-107">ByVirtualHubResourceId</span></span>

```powershell
New-AzVHubRouteTable -ParentResourceId <String> -Name <String> -Route <PSVHubRoute[]> -Label <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7879-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7879-108">DESCRIPTION</span></span>
<span data-ttu-id="f7879-109">Létrehozza a megadott virtuális központhoz társított útvonaltáblát a megadott útvonalokkal és címkékkel.</span><span class="sxs-lookup"><span data-stu-id="f7879-109">Creates the specified route table that is associated with the specified virtual hub with the provided routes and the labels.</span></span>

## <span data-ttu-id="f7879-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7879-110">EXAMPLES</span></span>

### <span data-ttu-id="f7879-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7879-111">Example 1</span></span>

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

Name                   : testRouteTable
Id                     : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/testRouteTable
ProvisioningState      : Succeeded
Labels                 : {testLabel}
Routes                 : [
                           {
                             "Name": "private-traffic",
                             "DestinationType": "CIDR",
                             "Destinations": [
                               "10.30.0.0/16",
                               "10.40.0.0/16"
                             ],
                             "NextHopType": "ResourceId",
                             "NextHop": "/subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall"
                           }
                         ]
AssociatedConnections  : []
PropagatingConnections : []
```

<span data-ttu-id="f7879-112">Ez a parancs létrehoz egy központi útválasztási táblát a virtuális központból.</span><span class="sxs-lookup"><span data-stu-id="f7879-112">This command creates a hub route table of the virtual hub.</span></span>

## <span data-ttu-id="f7879-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7879-113">PARAMETERS</span></span>

### <span data-ttu-id="f7879-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7879-114">-AsJob</span></span>
<span data-ttu-id="f7879-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f7879-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7879-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7879-116">-DefaultProfile</span></span>
<span data-ttu-id="f7879-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7879-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7879-118">-Label</span><span class="sxs-lookup"><span data-stu-id="f7879-118">-Label</span></span>
<span data-ttu-id="f7879-119">A címkék listája.</span><span class="sxs-lookup"><span data-stu-id="f7879-119">The list of labels.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7879-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f7879-120">-Name</span></span>
<span data-ttu-id="f7879-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f7879-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7879-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7879-122">-ParentObject</span></span>
<span data-ttu-id="f7879-123">Az erőforrás szülő virtuális központi objektuma.</span><span class="sxs-lookup"><span data-stu-id="f7879-123">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="f7879-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f7879-124">-ParentResourceName</span></span>
<span data-ttu-id="f7879-125">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f7879-125">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7879-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7879-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7879-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7879-127">The resource group name.</span></span>

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

### <span data-ttu-id="f7879-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f7879-128">-ParentResourceId</span></span>
<span data-ttu-id="f7879-129">A virtuális központi erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7879-129">The resource id of the virtual hub resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7879-130">-Útvonal</span><span class="sxs-lookup"><span data-stu-id="f7879-130">-Route</span></span>
<span data-ttu-id="f7879-131">Az útvonaltáblához az útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="f7879-131">The list of routes for this route table.</span></span>

```yaml
Type: PSVHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7879-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7879-132">-Confirm</span></span>
<span data-ttu-id="f7879-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7879-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7879-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7879-134">-WhatIf</span></span>
<span data-ttu-id="f7879-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7879-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7879-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7879-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7879-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7879-137">CommonParameters</span></span>
<span data-ttu-id="f7879-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7879-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7879-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7879-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7879-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7879-140">INPUTS</span></span>

### <span data-ttu-id="f7879-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f7879-141">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f7879-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-142">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="f7879-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f7879-143">System.String</span></span>

## <span data-ttu-id="f7879-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7879-144">OUTPUTS</span></span>

### <span data-ttu-id="f7879-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

## <span data-ttu-id="f7879-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7879-146">NOTES</span></span>

## <span data-ttu-id="f7879-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7879-147">RELATED LINKS</span></span>

[<span data-ttu-id="f7879-148">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-148">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="f7879-149">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="f7879-149">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="f7879-150">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-150">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="f7879-151">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7879-151">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)
