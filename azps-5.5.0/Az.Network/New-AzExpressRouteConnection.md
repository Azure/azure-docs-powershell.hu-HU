---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146947"
---
# <span data-ttu-id="e7aa5-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e7aa5-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="e7aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aa5-103">ExpressRoute-kapcsolatot hoz létre, amely egy ExpressRoute-átjárót egy távoli ExpressRoute-áramkörhöz csatlakoztat.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="e7aa5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7aa5-104">SYNTAX</span></span>

### <span data-ttu-id="e7aa5-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7aa5-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7aa5-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e7aa5-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7aa5-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e7aa5-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7aa5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7aa5-108">DESCRIPTION</span></span>
<span data-ttu-id="e7aa5-109">ExpressRoute-kapcsolatot hoz létre egy BGP-áramkör és az ExpressRoute-átjáró között egy virtuális központban.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="e7aa5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7aa5-110">EXAMPLES</span></span>

### <span data-ttu-id="e7aa5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e7aa5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="e7aa5-112">A fentiek létrehoznak egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway) és egy ExpressRoute-áramkört, amely az Azure "testRG" erőforráscsoportjaként a közép-amerikai Egyesült Államok nyugati részén privát társviszonyt létesít.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e7aa5-113">Miután létrehozta az átjárót, a kapcsolat az ExpressRoute-áramkör társviszony-létesítésében New-AzExpressRouteConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="e7aa5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7aa5-114">PARAMETERS</span></span>

### <span data-ttu-id="e7aa5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7aa5-115">-AsJob</span></span>
<span data-ttu-id="e7aa5-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e7aa5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7aa5-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="e7aa5-117">-AuthorizationKey</span></span>
<span data-ttu-id="e7aa5-118">Az ExpressRoute-kapcsolat kapcsolattulajdonosától kapott kulcs, hogy kapcsolatot létesítsen egy másik előfizetésben használt átjáróval.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="e7aa5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aa5-119">-DefaultProfile</span></span>
<span data-ttu-id="e7aa5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7aa5-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e7aa5-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="e7aa5-122">Az internetbiztonság engedélyezése ehhez az ExpressRoute-átjárókapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e7aa5-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="e7aa5-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="e7aa5-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="e7aa5-124">Annak az Express Route Circuit-társviszonynak az erőforrás-azonosítója, amelyhez az Express Route átjárókapcsolatot létre kell hozatni.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="e7aa5-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="e7aa5-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="e7aa5-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e7aa5-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="e7aa5-128">A kapcsolat szülő ExpressRouteGatewayje.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e7aa5-129">-Name</span></span>
<span data-ttu-id="e7aa5-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e7aa5-131">-ParentResourceId</span></span>
<span data-ttu-id="e7aa5-132">A kapcsolathoz a szülő ExpressRouteGateway erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aa5-133">-ResourceGroupName</span></span>
<span data-ttu-id="e7aa5-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7aa5-135">-RoutingConfiguration</span></span>
<span data-ttu-id="e7aa5-136">Útválasztási konfiguráció ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e7aa5-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="e7aa5-137">-RoutingWeight</span></span>
<span data-ttu-id="e7aa5-138">A kapcsolathoz hozzárendelni szükséges csomagtovább kapcsolat súlyát.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aa5-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7aa5-139">-Confirm</span></span>
<span data-ttu-id="e7aa5-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7aa5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7aa5-141">-WhatIf</span></span>
<span data-ttu-id="e7aa5-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7aa5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7aa5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aa5-144">CommonParameters</span></span>
<span data-ttu-id="e7aa5-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7aa5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aa5-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7aa5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aa5-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7aa5-147">INPUTS</span></span>

### <span data-ttu-id="e7aa5-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="e7aa5-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="e7aa5-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e7aa5-149">System.String</span></span>

## <span data-ttu-id="e7aa5-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7aa5-150">OUTPUTS</span></span>

### <span data-ttu-id="e7aa5-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e7aa5-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e7aa5-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7aa5-152">NOTES</span></span>

## <span data-ttu-id="e7aa5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7aa5-153">RELATED LINKS</span></span>

[<span data-ttu-id="e7aa5-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7aa5-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
