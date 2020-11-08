---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184368"
---
# <span data-ttu-id="40fb7-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="40fb7-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="40fb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="40fb7-103">Olyan ExpressRoute-kapcsolatot hoz létre, amely az ExpressRoute átjárót egy helyszíni ExpressRoute-áramkörhöz köti</span><span class="sxs-lookup"><span data-stu-id="40fb7-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="40fb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40fb7-104">SYNTAX</span></span>

### <span data-ttu-id="40fb7-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40fb7-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40fb7-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="40fb7-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40fb7-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="40fb7-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fb7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="40fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="40fb7-109">Létrejön egy ExpressRoute-kapcsolat az egy helyszíni ExpressRoute-áramkört, amely egy virtuális csomóponton belül a ExpressRoute-átjáróhoz csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="40fb7-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="40fb7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="40fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="40fb7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="40fb7-111">Example 1</span></span>

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

<span data-ttu-id="40fb7-112">A fentiekben létrehozunk egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub, expressz útvonal-átjáró és egy ExpressRoute-áramkör a közép-Közép-amerikai "testRG" erőforráscsoporthoz az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="40fb7-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="40fb7-113">Miután létrehozta az átjárót, az a New-AzExpressRouteConnection parancs segítségével csatlakozik az ExpressRoute-Áramkörhez.</span><span class="sxs-lookup"><span data-stu-id="40fb7-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="40fb7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40fb7-114">PARAMETERS</span></span>

### <span data-ttu-id="40fb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40fb7-115">-AsJob</span></span>
<span data-ttu-id="40fb7-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40fb7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40fb7-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="40fb7-117">-AuthorizationKey</span></span>
<span data-ttu-id="40fb7-118">Az ExpressRoute-áramkör tulajdonosa által kapott kulcs egy másik előfizetésben lévő átjáróval való kapcsolat létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="40fb7-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="40fb7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fb7-119">-DefaultProfile</span></span>
<span data-ttu-id="40fb7-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40fb7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40fb7-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="40fb7-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="40fb7-122">Az Internet biztonságának engedélyezése ehhez a ExpressRoute átjáró-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="40fb7-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="40fb7-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="40fb7-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="40fb7-124">Annak az Express Route-áramkörnek az erőforrás-azonosítója, amelyhez az útvonal-átjáró kapcsolata jön létre.</span><span class="sxs-lookup"><span data-stu-id="40fb7-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="40fb7-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="40fb7-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="40fb7-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="40fb7-126">The resource group name.</span></span>

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

### <span data-ttu-id="40fb7-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="40fb7-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="40fb7-128">A kapcsolat fölérendelt ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="40fb7-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="40fb7-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40fb7-129">-Name</span></span>
<span data-ttu-id="40fb7-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="40fb7-130">The resource name.</span></span>

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

### <span data-ttu-id="40fb7-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40fb7-131">-ParentResourceId</span></span>
<span data-ttu-id="40fb7-132">A kapcsolat fölérendelt ExpressRouteGateway tartozó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="40fb7-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="40fb7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fb7-133">-ResourceGroupName</span></span>
<span data-ttu-id="40fb7-134">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="40fb7-134">The resource group name.</span></span>

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

### <span data-ttu-id="40fb7-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="40fb7-135">-RoutingConfiguration</span></span>
<span data-ttu-id="40fb7-136">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="40fb7-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="40fb7-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="40fb7-137">-RoutingWeight</span></span>
<span data-ttu-id="40fb7-138">Annak a csomagnak az útválasztási tömege, amelyet ehhez a kapcsolathoz kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="40fb7-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="40fb7-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40fb7-139">-Confirm</span></span>
<span data-ttu-id="40fb7-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40fb7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fb7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fb7-141">-WhatIf</span></span>
<span data-ttu-id="40fb7-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40fb7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40fb7-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40fb7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fb7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fb7-144">CommonParameters</span></span>
<span data-ttu-id="40fb7-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40fb7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fb7-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40fb7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fb7-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40fb7-147">INPUTS</span></span>

### <span data-ttu-id="40fb7-148">Microsoft. Azure. commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="40fb7-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="40fb7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="40fb7-149">System.String</span></span>

## <span data-ttu-id="40fb7-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40fb7-150">OUTPUTS</span></span>

### <span data-ttu-id="40fb7-151">Microsoft. Azure. commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="40fb7-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="40fb7-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40fb7-152">NOTES</span></span>

## <span data-ttu-id="40fb7-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40fb7-153">RELATED LINKS</span></span>

[<span data-ttu-id="40fb7-154">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="40fb7-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
