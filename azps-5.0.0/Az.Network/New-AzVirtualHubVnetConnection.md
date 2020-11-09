---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301850"
---
# <span data-ttu-id="e6cd8-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e6cd8-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e6cd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cd8-103">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e6cd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6cd8-104">SYNTAX</span></span>

### <span data-ttu-id="e6cd8-105">ByVirtualHubNameByRemoteVirtualNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6cd8-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e6cd8-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e6cd8-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cd8-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6cd8-111">DESCRIPTION</span></span>
<span data-ttu-id="e6cd8-112">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e6cd8-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e6cd8-113">EXAMPLES</span></span>

### <span data-ttu-id="e6cd8-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6cd8-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
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

<span data-ttu-id="e6cd8-115">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e6cd8-116">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="e6cd8-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6cd8-117">Example 2</span></span>

<span data-ttu-id="e6cd8-118">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="e6cd8-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="e6cd8-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="e6cd8-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="e6cd8-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="e6cd8-121">A fenti művelet új útválasztási konfigurációt hoz létre, és statikus útvonalakat hoz létre az útválasztási konfigurációban a következő ugrással megadott IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="e6cd8-122">Ezt az útválasztási konfigurációt ezután átadhatja a New-AzVirtualHubVnetConnection parancsnak a paraméter-RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="e6cd8-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6cd8-123">PARAMETERS</span></span>

### <span data-ttu-id="e6cd8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6cd8-124">-AsJob</span></span>
<span data-ttu-id="e6cd8-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e6cd8-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6cd8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cd8-126">-DefaultProfile</span></span>
<span data-ttu-id="e6cd8-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cd8-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e6cd8-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="e6cd8-129">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e6cd8-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="e6cd8-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="e6cd8-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="e6cd8-131">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e6cd8-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6cd8-132">-Name</span></span>
<span data-ttu-id="e6cd8-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e6cd8-134">-ParentObject</span></span>
<span data-ttu-id="e6cd8-135">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-136">-ParentResourceId</span></span>
<span data-ttu-id="e6cd8-137">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e6cd8-138">-ParentResourceName</span></span>
<span data-ttu-id="e6cd8-139">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6cd8-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="e6cd8-141">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="e6cd8-143">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cd8-144">-ResourceGroupName</span></span>
<span data-ttu-id="e6cd8-145">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd8-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6cd8-146">-RoutingConfiguration</span></span>
<span data-ttu-id="e6cd8-147">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="e6cd8-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="e6cd8-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6cd8-148">-Confirm</span></span>
<span data-ttu-id="e6cd8-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cd8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cd8-150">-WhatIf</span></span>
<span data-ttu-id="e6cd8-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cd8-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cd8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cd8-153">CommonParameters</span></span>
<span data-ttu-id="e6cd8-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6cd8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cd8-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cd8-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cd8-156">INPUTS</span></span>

### <span data-ttu-id="e6cd8-157">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e6cd8-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e6cd8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e6cd8-158">System.String</span></span>

## <span data-ttu-id="e6cd8-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6cd8-159">OUTPUTS</span></span>

### <span data-ttu-id="e6cd8-160">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e6cd8-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e6cd8-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6cd8-161">NOTES</span></span>

## <span data-ttu-id="e6cd8-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6cd8-162">RELATED LINKS</span></span>

[<span data-ttu-id="e6cd8-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e6cd8-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e6cd8-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e6cd8-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e6cd8-165">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6cd8-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
