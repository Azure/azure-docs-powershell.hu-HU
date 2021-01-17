---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481107"
---
# <span data-ttu-id="2b479-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2b479-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="2b479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b479-102">SYNOPSIS</span></span>
<span data-ttu-id="2b479-103">Egy meglévő HubVirtualNetworkConnection frissítése.</span><span class="sxs-lookup"><span data-stu-id="2b479-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="2b479-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b479-104">SYNTAX</span></span>

### <span data-ttu-id="2b479-105">ByHubVirtualNetworkConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b479-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b479-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2b479-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b479-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="2b479-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b479-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b479-108">DESCRIPTION</span></span>
<span data-ttu-id="2b479-109">Egy meglévő HubVirtualNetworkConnection frissítése.</span><span class="sxs-lookup"><span data-stu-id="2b479-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="2b479-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b479-110">EXAMPLES</span></span>

### <span data-ttu-id="2b479-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2b479-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="2b479-112">A fentiekkel az Azure-ban az adott erőforráscsoportban létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US).</span><span class="sxs-lookup"><span data-stu-id="2b479-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="2b479-113">Létrejön egy virtuális hálózati kapcsolat is, amely a virtuális hálózat és a virtuális központ közötti társközi kapcsolat.</span><span class="sxs-lookup"><span data-stu-id="2b479-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="2b479-114">A virtuális hálózati kapcsolat ekkor frissül az internetbiztonság engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="2b479-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="2b479-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b479-115">PARAMETERS</span></span>

### <span data-ttu-id="2b479-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b479-116">-AsJob</span></span>
<span data-ttu-id="2b479-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2b479-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b479-118">-DefaultProfile</span></span>
<span data-ttu-id="2b479-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b479-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2b479-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="2b479-121">Engedélyezze az internetbiztonságot ehhez a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="2b479-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="2b479-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b479-122">-InputObject</span></span>
<span data-ttu-id="2b479-123">A hubvirtualnetworkconnection resource to modify.</span><span class="sxs-lookup"><span data-stu-id="2b479-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2b479-124">-Name</span></span>
<span data-ttu-id="2b479-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2b479-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="2b479-126">-ParentResourceName</span></span>
<span data-ttu-id="2b479-127">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2b479-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b479-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b479-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2b479-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b479-130">-ResourceId</span></span>
<span data-ttu-id="2b479-131">A módosítani szükséges hubvirtualnetworkconnection erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2b479-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b479-132">-RoutingConfiguration</span></span>
<span data-ttu-id="2b479-133">Útválasztási konfiguráció ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="2b479-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="2b479-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b479-134">-Confirm</span></span>
<span data-ttu-id="2b479-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2b479-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b479-136">-WhatIf</span></span>
<span data-ttu-id="2b479-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2b479-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b479-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b479-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b479-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b479-139">CommonParameters</span></span>
<span data-ttu-id="2b479-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b479-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b479-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b479-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b479-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b479-142">INPUTS</span></span>

### <span data-ttu-id="2b479-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2b479-143">System.String</span></span>

### <span data-ttu-id="2b479-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="2b479-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="2b479-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b479-145">OUTPUTS</span></span>

### <span data-ttu-id="2b479-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="2b479-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="2b479-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b479-147">NOTES</span></span>

## <span data-ttu-id="2b479-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b479-148">RELATED LINKS</span></span>

[<span data-ttu-id="2b479-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b479-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
