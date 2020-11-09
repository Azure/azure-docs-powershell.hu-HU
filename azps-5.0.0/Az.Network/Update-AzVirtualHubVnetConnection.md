---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303052"
---
# <span data-ttu-id="b41b9-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b41b9-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="b41b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b41b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b41b9-103">Frissít egy meglévő HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="b41b9-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b41b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b41b9-104">SYNTAX</span></span>

### <span data-ttu-id="b41b9-105">ByHubVirtualNetworkConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b41b9-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b41b9-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b41b9-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b41b9-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b41b9-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b41b9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b41b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b41b9-109">Frissít egy meglévő HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="b41b9-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b41b9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b41b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b41b9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b41b9-111">Example 1</span></span>
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

<span data-ttu-id="b41b9-112">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="b41b9-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b41b9-113">Virtuális hálózati kapcsolat jön létre, amely a virtuális központhoz tartozó virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="b41b9-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="b41b9-114">Ez a virtuális hálózati kapcsolat az internetes biztonság engedélyezését követően frissül.</span><span class="sxs-lookup"><span data-stu-id="b41b9-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="b41b9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b41b9-115">PARAMETERS</span></span>

### <span data-ttu-id="b41b9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b41b9-116">-AsJob</span></span>
<span data-ttu-id="b41b9-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b41b9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b41b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41b9-118">-DefaultProfile</span></span>
<span data-ttu-id="b41b9-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b41b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b41b9-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="b41b9-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="b41b9-121">Engedélyezze az internetes biztonságot ehhez a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="b41b9-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="b41b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b41b9-122">-InputObject</span></span>
<span data-ttu-id="b41b9-123">A módosítani kívánt hubvirtualnetworkconnection-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b41b9-123">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b41b9-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b41b9-124">-Name</span></span>
<span data-ttu-id="b41b9-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b41b9-125">The resource name.</span></span>

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

### <span data-ttu-id="b41b9-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b41b9-126">-ParentResourceName</span></span>
<span data-ttu-id="b41b9-127">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b41b9-127">The parent resource name.</span></span>

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

### <span data-ttu-id="b41b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="b41b9-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b41b9-129">The resource group name.</span></span>

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

### <span data-ttu-id="b41b9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b41b9-130">-ResourceId</span></span>
<span data-ttu-id="b41b9-131">A módosítandó hubvirtualnetworkconnection erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b41b9-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b41b9-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b41b9-132">-RoutingConfiguration</span></span>
<span data-ttu-id="b41b9-133">A kapcsolat útválasztási konfigurációja</span><span class="sxs-lookup"><span data-stu-id="b41b9-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="b41b9-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b41b9-134">-Confirm</span></span>
<span data-ttu-id="b41b9-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b41b9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b41b9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b41b9-136">-WhatIf</span></span>
<span data-ttu-id="b41b9-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b41b9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b41b9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b41b9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b41b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41b9-139">CommonParameters</span></span>
<span data-ttu-id="b41b9-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b41b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41b9-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41b9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41b9-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41b9-142">INPUTS</span></span>

### <span data-ttu-id="b41b9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b41b9-143">System.String</span></span>

### <span data-ttu-id="b41b9-144">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="b41b9-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="b41b9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41b9-145">OUTPUTS</span></span>

### <span data-ttu-id="b41b9-146">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="b41b9-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="b41b9-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b41b9-147">NOTES</span></span>

## <span data-ttu-id="b41b9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b41b9-148">RELATED LINKS</span></span>

[<span data-ttu-id="b41b9-149">Új – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b41b9-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
