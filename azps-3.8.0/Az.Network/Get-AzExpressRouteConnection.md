---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 9c1d07a8e8c02b57a67b009f0ebe438134d7d56c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013463"
---
# <span data-ttu-id="cb564-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb564-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="cb564-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb564-102">SYNOPSIS</span></span>
<span data-ttu-id="cb564-103">ExpressRoute-kapcsolatot kap név vagy a ExpressRouteGateway csatlakoztatott összes ExpressRoute-kapcsolat esetén.</span><span class="sxs-lookup"><span data-stu-id="cb564-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="cb564-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb564-104">SYNTAX</span></span>

### <span data-ttu-id="cb564-105">ByExpressRouteGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb564-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb564-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cb564-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb564-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cb564-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb564-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb564-108">DESCRIPTION</span></span>
<span data-ttu-id="cb564-109">Beolvassa a ExpressRoute kapcsolatot név szerint, vagy felsorolja a ExpressRouteGateway csatlakoztatott összes ExpressRoute-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="cb564-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="cb564-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cb564-110">EXAMPLES</span></span>

### <span data-ttu-id="cb564-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb564-111">Example 1</span></span>

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
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="cb564-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub és egy ExpressRouteSite a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="cb564-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cb564-113">Ezt követően egy ExpressRoute átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="cb564-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cb564-114">Miután létrehozta az átjárót, az a New-AzExpressRouteConnection parancs segítségével csatlakozik a helyszíni ExpressRoute-áramkörhez.</span><span class="sxs-lookup"><span data-stu-id="cb564-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="cb564-115">Ezután a kapcsolat neve alapján kapja meg a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="cb564-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="cb564-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="cb564-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="cb564-117">Ez a parancs a "teszt" kezdetű "testExpressRoutegw" ExpressRoute minden kapcsolatát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="cb564-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="cb564-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb564-118">PARAMETERS</span></span>

### <span data-ttu-id="cb564-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb564-119">-DefaultProfile</span></span>
<span data-ttu-id="cb564-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb564-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb564-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="cb564-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="cb564-122">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cb564-122">The parent resource name.</span></span>

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

### <span data-ttu-id="cb564-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cb564-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="cb564-124">A kapcsolat fölérendelt ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="cb564-124">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="cb564-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb564-125">-Name</span></span>
<span data-ttu-id="cb564-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cb564-126">The resource name.</span></span>

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

### <span data-ttu-id="cb564-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb564-127">-ParentResourceId</span></span>
<span data-ttu-id="cb564-128">A kapcsolat fölérendelt ExpressRouteGateway tartozó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cb564-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="cb564-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb564-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb564-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb564-130">The resource group name.</span></span>

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

### <span data-ttu-id="cb564-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb564-131">CommonParameters</span></span>
<span data-ttu-id="cb564-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb564-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb564-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb564-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb564-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb564-134">INPUTS</span></span>

### <span data-ttu-id="cb564-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cb564-135">System.String</span></span>

## <span data-ttu-id="cb564-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb564-136">OUTPUTS</span></span>

### <span data-ttu-id="cb564-137">Microsoft. Azure. commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cb564-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="cb564-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb564-138">NOTES</span></span>

## <span data-ttu-id="cb564-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb564-139">RELATED LINKS</span></span>
