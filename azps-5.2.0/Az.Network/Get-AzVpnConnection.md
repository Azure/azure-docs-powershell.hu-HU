---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 6ad7f5fcdaafed47d7292444370e332188f444b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369905"
---
# <span data-ttu-id="fb4bc-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb4bc-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="fb4bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4bc-103">Vpn-kapcsolatot kap név szerint, vagy felsorolja a VpnGatewayhez csatlakoztatott összes VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="fb4bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb4bc-104">SYNTAX</span></span>

### <span data-ttu-id="fb4bc-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb4bc-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="fb4bc-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb4bc-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="fb4bc-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb4bc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb4bc-108">DESCRIPTION</span></span>
<span data-ttu-id="fb4bc-109">Vpn-kapcsolatot kap név szerint, vagy felsorolja a VpnGatewayhez csatlakoztatott összes VPN-kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="fb4bc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb4bc-110">EXAMPLES</span></span>

### <span data-ttu-id="fb4bc-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fb4bc-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="fb4bc-112">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub és VpnSite in West US in "testRG" resource group in Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fb4bc-113">Ezután létrejön egy VPN-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fb4bc-114">Miután létrehozta az átjárót, a virtuális magánhálózathoz csatlakozik a New-AzVpnConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fb4bc-115">Ezután a kapcsolatot a kapcsolat nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="fb4bc-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="fb4bc-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="fb4bc-117">Ez a parancsmag az összes olyan kapcsolatot beveszi, amely a "teszt" kezdetsel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="fb4bc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb4bc-118">PARAMETERS</span></span>

### <span data-ttu-id="fb4bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4bc-119">-DefaultProfile</span></span>
<span data-ttu-id="fb4bc-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb4bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fb4bc-121">-Name</span></span>
<span data-ttu-id="fb4bc-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4bc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb4bc-123">-ParentObject</span></span>
<span data-ttu-id="fb4bc-124">A kapcsolathoz a szülő VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4bc-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb4bc-125">-ParentResourceId</span></span>
<span data-ttu-id="fb4bc-126">A kapcsolathoz a szülő VpnGateway erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4bc-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fb4bc-127">-ParentResourceName</span></span>
<span data-ttu-id="fb4bc-128">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4bc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4bc-129">-ResourceGroupName</span></span>
<span data-ttu-id="fb4bc-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4bc-131">CommonParameters</span></span>
<span data-ttu-id="fb4bc-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4bc-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb4bc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4bc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb4bc-134">INPUTS</span></span>

### <span data-ttu-id="fb4bc-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fb4bc-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="fb4bc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fb4bc-136">System.String</span></span>

## <span data-ttu-id="fb4bc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4bc-137">OUTPUTS</span></span>

### <span data-ttu-id="fb4bc-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb4bc-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fb4bc-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb4bc-139">NOTES</span></span>

## <span data-ttu-id="fb4bc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb4bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="fb4bc-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb4bc-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="fb4bc-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb4bc-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="fb4bc-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fb4bc-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
