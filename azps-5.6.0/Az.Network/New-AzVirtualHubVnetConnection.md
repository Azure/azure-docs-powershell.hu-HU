---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 42592e1d72303c98a27890e2ac7721d95c37f928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926513"
---
# <span data-ttu-id="e79ee-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e79ee-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="e79ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e79ee-102">SYNOPSIS</span></span>
<span data-ttu-id="e79ee-103">A New-AzVirtualHubVnetConnection parancsmag létrehoz egy HubVirtualNetworkConnection erőforrást, amely virtuális hálózattal csatlakozik az Azure Virtual Hubhoz.</span><span class="sxs-lookup"><span data-stu-id="e79ee-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e79ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e79ee-104">SYNTAX</span></span>

### <span data-ttu-id="e79ee-105">ByVirtualHubNameByRemoteVirtualNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e79ee-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e79ee-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e79ee-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e79ee-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e79ee-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e79ee-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e79ee-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e79ee-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="e79ee-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e79ee-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e79ee-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e79ee-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e79ee-111">DESCRIPTION</span></span>
<span data-ttu-id="e79ee-112">A New-AzVirtualHubVnetConnection parancsmag létrehoz egy HubVirtualNetworkConnection erőforrást, amely virtuális hálózattal csatlakozik az Azure Virtual Hubhoz.</span><span class="sxs-lookup"><span data-stu-id="e79ee-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="e79ee-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e79ee-113">EXAMPLES</span></span>

### <span data-ttu-id="e79ee-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="e79ee-114">Example 1</span></span>

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

<span data-ttu-id="e79ee-115">A fentiekkel az Azure-ban az adott erőforráscsoportban létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US).</span><span class="sxs-lookup"><span data-stu-id="e79ee-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="e79ee-116">Ezután létrejön egy virtuális hálózati kapcsolat, amely a virtuális hálózat és a virtuális központ közötti társviszonyba fog hozni.</span><span class="sxs-lookup"><span data-stu-id="e79ee-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="e79ee-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="e79ee-117">Example 2</span></span>

<span data-ttu-id="e79ee-118">A New-AzVirtualHubVnetConnection parancsmag létrehoz egy HubVirtualNetworkConnection erőforrást, amely virtuális hálózattal csatlakozik az Azure Virtual Hubhoz.</span><span class="sxs-lookup"><span data-stu-id="e79ee-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="e79ee-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="e79ee-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="e79ee-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="e79ee-120">Example 3</span></span>
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
<span data-ttu-id="e79ee-121">A fenti új útválasztási konfigurációt hoz létre, és statikus útvonalakat hoz létre az útválasztási konfigurációban, a következő ugrással a megadott IP-címként.</span><span class="sxs-lookup"><span data-stu-id="e79ee-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="e79ee-122">Ezt az útválasztási konfigurációt ezután a New-AzVirtualHubVnetConnection paraméter -RoutingConfiguration paraméterként lehet átadva a New-AzVirtualHubVnetConnection parancsnak.</span><span class="sxs-lookup"><span data-stu-id="e79ee-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="e79ee-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e79ee-123">PARAMETERS</span></span>

### <span data-ttu-id="e79ee-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e79ee-124">-AsJob</span></span>
<span data-ttu-id="e79ee-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e79ee-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e79ee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79ee-126">-DefaultProfile</span></span>
<span data-ttu-id="e79ee-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e79ee-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e79ee-128">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e79ee-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="e79ee-129">Az internetbiztonság engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e79ee-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="e79ee-130">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="e79ee-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="e79ee-131">Az internetbiztonság engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e79ee-131">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="e79ee-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e79ee-132">-Name</span></span>
<span data-ttu-id="e79ee-133">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e79ee-133">The resource name.</span></span>

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

### <span data-ttu-id="e79ee-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e79ee-134">-ParentObject</span></span>
<span data-ttu-id="e79ee-135">A szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="e79ee-135">The parent resource.</span></span>

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

### <span data-ttu-id="e79ee-136">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e79ee-136">-ParentResourceId</span></span>
<span data-ttu-id="e79ee-137">A szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="e79ee-137">The parent resource.</span></span>

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

### <span data-ttu-id="e79ee-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="e79ee-138">-ParentResourceName</span></span>
<span data-ttu-id="e79ee-139">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e79ee-139">The resource group name.</span></span>

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

### <span data-ttu-id="e79ee-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e79ee-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="e79ee-141">Az a távoli virtuális hálózat, amelyhez ez a központi virtuális hálózati kapcsolat kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="e79ee-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="e79ee-142">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e79ee-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="e79ee-143">Az a távoli virtuális hálózat, amelyhez ez a központi virtuális hálózati kapcsolat kapcsolódik.</span><span class="sxs-lookup"><span data-stu-id="e79ee-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="e79ee-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e79ee-144">-ResourceGroupName</span></span>
<span data-ttu-id="e79ee-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e79ee-145">The resource group name.</span></span>

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

### <span data-ttu-id="e79ee-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e79ee-146">-RoutingConfiguration</span></span>
<span data-ttu-id="e79ee-147">Útválasztási konfiguráció ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="e79ee-147">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="e79ee-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e79ee-148">-Confirm</span></span>
<span data-ttu-id="e79ee-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e79ee-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e79ee-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e79ee-150">-WhatIf</span></span>
<span data-ttu-id="e79ee-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e79ee-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e79ee-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e79ee-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e79ee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79ee-153">CommonParameters</span></span>
<span data-ttu-id="e79ee-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e79ee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79ee-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e79ee-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79ee-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e79ee-156">INPUTS</span></span>

### <span data-ttu-id="e79ee-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e79ee-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e79ee-158">System.String</span><span class="sxs-lookup"><span data-stu-id="e79ee-158">System.String</span></span>

## <span data-ttu-id="e79ee-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e79ee-159">OUTPUTS</span></span>

### <span data-ttu-id="e79ee-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="e79ee-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="e79ee-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e79ee-161">NOTES</span></span>

## <span data-ttu-id="e79ee-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e79ee-162">RELATED LINKS</span></span>

[<span data-ttu-id="e79ee-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e79ee-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e79ee-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e79ee-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="e79ee-165">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e79ee-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
