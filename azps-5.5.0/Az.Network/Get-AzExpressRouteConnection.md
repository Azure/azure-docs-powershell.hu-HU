---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 10514c693ff349550ee2c751f2a3091a7211a41e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154443"
---
# <span data-ttu-id="4c3e8-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4c3e8-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="4c3e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3e8-103">ExpressRoute-kapcsolatot kap név szerint, vagy felsorolja az ExpressRouteGatewayhez csatlakoztatott összes ExpressRoute-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="4c3e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c3e8-104">SYNTAX</span></span>

### <span data-ttu-id="4c3e8-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c3e8-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c3e8-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4c3e8-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c3e8-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4c3e8-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c3e8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c3e8-108">DESCRIPTION</span></span>
<span data-ttu-id="4c3e8-109">ExpressRoute-kapcsolatot kap név szerint, vagy felsorolja az ExpressRouteGatewayhez csatlakoztatott összes ExpressRoute-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="4c3e8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c3e8-110">EXAMPLES</span></span>

### <span data-ttu-id="4c3e8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4c3e8-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
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

<span data-ttu-id="4c3e8-112">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és ExpressRouteSite, Nyugat-Egyesült Államok) az Azure "testRG" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4c3e8-113">Ezután létrejön egy ExpressRoute-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4c3e8-114">Miután létrehozta az átjárót, az a New-AzExpressRouteConnection paranccsal csatlakozik a New-AzExpressRouteConnection ExpressRoute-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="4c3e8-115">Ezután a kapcsolatot a kapcsolat nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="4c3e8-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="4c3e8-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
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

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
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

<span data-ttu-id="4c3e8-117">Ez a parancs az ExpressRoute "testExpressRoutegw" minden olyan kapcsolatát be fogja szerezni, amely a "test" kezdetsel kezdődik</span><span class="sxs-lookup"><span data-stu-id="4c3e8-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="4c3e8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c3e8-118">PARAMETERS</span></span>

### <span data-ttu-id="4c3e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3e8-119">-DefaultProfile</span></span>
<span data-ttu-id="4c3e8-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e8-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="4c3e8-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="4c3e8-122">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e8-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4c3e8-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="4c3e8-124">A kapcsolat szülő ExpressRouteGatewayje.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4c3e8-125">-Name</span></span>
<span data-ttu-id="4c3e8-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4c3e8-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4c3e8-127">-ParentResourceId</span></span>
<span data-ttu-id="4c3e8-128">A kapcsolathoz a szülő ExpressRouteGateway erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="4c3e8-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c3e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3e8-131">CommonParameters</span></span>
<span data-ttu-id="4c3e8-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c3e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3e8-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c3e8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3e8-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c3e8-134">INPUTS</span></span>

### <span data-ttu-id="4c3e8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4c3e8-135">System.String</span></span>

## <span data-ttu-id="4c3e8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c3e8-136">OUTPUTS</span></span>

### <span data-ttu-id="4c3e8-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4c3e8-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="4c3e8-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c3e8-138">NOTES</span></span>

## <span data-ttu-id="4c3e8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c3e8-139">RELATED LINKS</span></span>
