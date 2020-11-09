---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301859"
---
# <span data-ttu-id="299bb-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="299bb-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="299bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="299bb-102">SYNOPSIS</span></span>
<span data-ttu-id="299bb-103">Létrehoz egy VHubRoute objektumot, amely paraméterként átadható a New-AzVHubRouteTable parancshoz.</span><span class="sxs-lookup"><span data-stu-id="299bb-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="299bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="299bb-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="299bb-105">DESCRIPTION</span></span>

<span data-ttu-id="299bb-106">VHubRoute objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="299bb-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="299bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="299bb-107">EXAMPLES</span></span>

### <span data-ttu-id="299bb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="299bb-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="299bb-109">A fenti parancs egy VHubRoute objektumot hoz létre a nextHop-ban, és a megadott tűzfalon keresztül hozzáadható egy VHubRouteTable-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="299bb-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="299bb-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="299bb-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="299bb-111">A fenti parancs egy VHubRoute objektumot hoz létre a nextHop megadott hubVnetConnection, melyet aztán hozzáadhat egy VHubRouteTable-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="299bb-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="299bb-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="299bb-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="299bb-113">A fenti parancsok bemutatják a már meglévő AzVHubRoute RoutingConfiguration, majd hozzáadhat egy statikus útvonalat a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="299bb-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="299bb-114">Azt is megteheti, hogy új kapcsolatot hoz létre a statikus útvonalon belül, az első példa [itt található.](New-AzRoutingConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="299bb-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="299bb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="299bb-115">PARAMETERS</span></span>

### <span data-ttu-id="299bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299bb-116">-DefaultProfile</span></span>
<span data-ttu-id="299bb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="299bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="299bb-118">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="299bb-118">-Destination</span></span>
<span data-ttu-id="299bb-119">A célhelyek listája.</span><span class="sxs-lookup"><span data-stu-id="299bb-119">List of Destinations.</span></span>

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

### <span data-ttu-id="299bb-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="299bb-120">-DestinationType</span></span>
<span data-ttu-id="299bb-121">A rendeltetési hely típusa.</span><span class="sxs-lookup"><span data-stu-id="299bb-121">Type of Destinations.</span></span>

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

### <span data-ttu-id="299bb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="299bb-122">-Name</span></span>
<span data-ttu-id="299bb-123">Az útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="299bb-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299bb-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="299bb-124">-NextHop</span></span>
<span data-ttu-id="299bb-125">A következő Ugrás elemre.</span><span class="sxs-lookup"><span data-stu-id="299bb-125">The next hop.</span></span>

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

### <span data-ttu-id="299bb-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="299bb-126">-NextHopType</span></span>
<span data-ttu-id="299bb-127">A következő ugrás típusa</span><span class="sxs-lookup"><span data-stu-id="299bb-127">The Next Hop type.</span></span>

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

### <span data-ttu-id="299bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299bb-128">CommonParameters</span></span>
<span data-ttu-id="299bb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="299bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299bb-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="299bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299bb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="299bb-131">INPUTS</span></span>

### <span data-ttu-id="299bb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="299bb-132">System.String</span></span>

## <span data-ttu-id="299bb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="299bb-133">OUTPUTS</span></span>

### <span data-ttu-id="299bb-134">Microsoft. Azure. commands. Network. models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="299bb-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="299bb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="299bb-135">NOTES</span></span>

## <span data-ttu-id="299bb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="299bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="299bb-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299bb-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="299bb-138">Új – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299bb-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="299bb-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299bb-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="299bb-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="299bb-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)