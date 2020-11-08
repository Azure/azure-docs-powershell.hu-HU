---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184361"
---
# <span data-ttu-id="f5168-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5168-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f5168-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5168-102">SYNOPSIS</span></span>
<span data-ttu-id="f5168-103">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="f5168-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f5168-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5168-104">SYNTAX</span></span>

### <span data-ttu-id="f5168-105">ByVirtualHubNameByRemoteVirtualNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5168-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5168-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f5168-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5168-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f5168-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5168-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f5168-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5168-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="f5168-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5168-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f5168-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5168-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5168-111">DESCRIPTION</span></span>
<span data-ttu-id="f5168-112">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="f5168-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="f5168-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f5168-113">EXAMPLES</span></span>

### <span data-ttu-id="f5168-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f5168-114">Example 1</span></span>

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

<span data-ttu-id="f5168-115">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="f5168-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f5168-116">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="f5168-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="f5168-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="f5168-117">Example 2</span></span>

<span data-ttu-id="f5168-118">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="f5168-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="f5168-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="f5168-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="f5168-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5168-120">PARAMETERS</span></span>

### <span data-ttu-id="f5168-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5168-121">-AsJob</span></span>
<span data-ttu-id="f5168-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f5168-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5168-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5168-123">-DefaultProfile</span></span>
<span data-ttu-id="f5168-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5168-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5168-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="f5168-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="f5168-126">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="f5168-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="f5168-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="f5168-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="f5168-128">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="f5168-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="f5168-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5168-129">-Name</span></span>
<span data-ttu-id="f5168-130">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f5168-130">The resource name.</span></span>

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

### <span data-ttu-id="f5168-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5168-131">-ParentObject</span></span>
<span data-ttu-id="f5168-132">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f5168-132">The parent resource.</span></span>

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

### <span data-ttu-id="f5168-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f5168-133">-ParentResourceId</span></span>
<span data-ttu-id="f5168-134">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f5168-134">The parent resource.</span></span>

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

### <span data-ttu-id="f5168-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f5168-135">-ParentResourceName</span></span>
<span data-ttu-id="f5168-136">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5168-136">The resource group name.</span></span>

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

### <span data-ttu-id="f5168-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f5168-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="f5168-138">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="f5168-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="f5168-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f5168-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="f5168-140">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="f5168-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="f5168-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5168-141">-ResourceGroupName</span></span>
<span data-ttu-id="f5168-142">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5168-142">The resource group name.</span></span>

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

### <span data-ttu-id="f5168-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5168-143">-RoutingConfiguration</span></span>
<span data-ttu-id="f5168-144">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="f5168-144">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="f5168-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5168-145">-Confirm</span></span>
<span data-ttu-id="f5168-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5168-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5168-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5168-147">-WhatIf</span></span>
<span data-ttu-id="f5168-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5168-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5168-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5168-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5168-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5168-150">CommonParameters</span></span>
<span data-ttu-id="f5168-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5168-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5168-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5168-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5168-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5168-153">INPUTS</span></span>

### <span data-ttu-id="f5168-154">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f5168-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f5168-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f5168-155">System.String</span></span>

## <span data-ttu-id="f5168-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5168-156">OUTPUTS</span></span>

### <span data-ttu-id="f5168-157">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f5168-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="f5168-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5168-158">NOTES</span></span>

## <span data-ttu-id="f5168-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5168-159">RELATED LINKS</span></span>

[<span data-ttu-id="f5168-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5168-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f5168-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f5168-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f5168-162">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5168-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
