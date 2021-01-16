---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 688168317a622cb0375bb111050f3e54696047ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356129"
---
# <span data-ttu-id="81310-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="81310-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="81310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81310-102">SYNOPSIS</span></span>
<span data-ttu-id="81310-103">Virtuális hálózati kapcsolatot kap egy virtuális központban, vagy felsorolja egy virtuális központ összes virtuális hálózati kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="81310-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="81310-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81310-104">SYNTAX</span></span>

### <span data-ttu-id="81310-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81310-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81310-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="81310-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81310-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="81310-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81310-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81310-108">DESCRIPTION</span></span>
<span data-ttu-id="81310-109">Virtuális hálózati kapcsolatot kap egy virtuális központban, vagy felsorolja egy virtuális központ összes virtuális hálózati kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="81310-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="81310-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81310-110">EXAMPLES</span></span>

### <span data-ttu-id="81310-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="81310-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="81310-112">A fentiekkel az Azure-ban az adott erőforráscsoportban létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US).</span><span class="sxs-lookup"><span data-stu-id="81310-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="81310-113">Ezután létrejön egy virtuális hálózati kapcsolat, amely a virtuális hálózat és a virtuális központ közötti társviszonyba fog hozni.</span><span class="sxs-lookup"><span data-stu-id="81310-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="81310-114">A központi virtuális hálózati kapcsolat létrehozása után a központi virtuális hálózati kapcsolatot az erőforráscsoport neve, a központ neve és a kapcsolat neve használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="81310-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="81310-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="81310-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="81310-116">A fentiekkel az Azure-ban az adott erőforráscsoportban létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US).</span><span class="sxs-lookup"><span data-stu-id="81310-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="81310-117">Ezután létrejön egy virtuális hálózati kapcsolat, amely a virtuális hálózat és a virtuális központ közötti társviszonyba fog hozni.</span><span class="sxs-lookup"><span data-stu-id="81310-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="81310-118">A központi virtuális hálózati kapcsolat létrehozása után felsorolja az összes központi virtuális hálózati kapcsolatot az erőforráscsoport és a központi név használatával.</span><span class="sxs-lookup"><span data-stu-id="81310-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="81310-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="81310-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
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

<span data-ttu-id="81310-120">Ez a parancsmag felsorolja az összes központi virtuális hálózati kapcsolatot a "teszt" szótól kezdve az erőforráscsoport és a központi név használatával.</span><span class="sxs-lookup"><span data-stu-id="81310-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="81310-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81310-121">PARAMETERS</span></span>

### <span data-ttu-id="81310-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81310-122">-DefaultProfile</span></span>
<span data-ttu-id="81310-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81310-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81310-124">-Name</span><span class="sxs-lookup"><span data-stu-id="81310-124">-Name</span></span>
<span data-ttu-id="81310-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="81310-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="81310-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81310-126">-ParentObject</span></span>
<span data-ttu-id="81310-127">A szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="81310-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81310-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="81310-128">-ParentResourceId</span></span>
<span data-ttu-id="81310-129">A szülőerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="81310-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81310-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="81310-130">-ParentResourceName</span></span>
<span data-ttu-id="81310-131">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="81310-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81310-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81310-132">-ResourceGroupName</span></span>
<span data-ttu-id="81310-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81310-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81310-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81310-134">CommonParameters</span></span>
<span data-ttu-id="81310-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81310-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81310-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81310-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81310-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81310-137">INPUTS</span></span>

### <span data-ttu-id="81310-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="81310-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="81310-139">System.String</span><span class="sxs-lookup"><span data-stu-id="81310-139">System.String</span></span>

## <span data-ttu-id="81310-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81310-140">OUTPUTS</span></span>

### <span data-ttu-id="81310-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="81310-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="81310-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81310-142">NOTES</span></span>

## <span data-ttu-id="81310-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81310-143">RELATED LINKS</span></span>

[<span data-ttu-id="81310-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="81310-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="81310-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="81310-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
