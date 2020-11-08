---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013237"
---
# <span data-ttu-id="a39c6-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a39c6-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="a39c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a39c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a39c6-103">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="a39c6-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="a39c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a39c6-104">SYNTAX</span></span>

### <span data-ttu-id="a39c6-105">ByVirtualHubNameByRemoteVirtualNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a39c6-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39c6-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a39c6-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39c6-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="a39c6-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39c6-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a39c6-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a39c6-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="a39c6-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39c6-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a39c6-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a39c6-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="a39c6-111">DESCRIPTION</span></span>
<span data-ttu-id="a39c6-112">Az New-AzVirtualHubVnetConnection parancsmag olyan HubVirtualNetworkConnection-erőforrást hoz létre, amely egy virtuális hálózatot hoz létre az Azure Virtual hub-hoz.</span><span class="sxs-lookup"><span data-stu-id="a39c6-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="a39c6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a39c6-113">EXAMPLES</span></span>

### <span data-ttu-id="a39c6-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a39c6-114">Example 1</span></span>

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
```

<span data-ttu-id="a39c6-115">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="a39c6-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="a39c6-116">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="a39c6-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="a39c6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a39c6-117">PARAMETERS</span></span>

### <span data-ttu-id="a39c6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a39c6-118">-AsJob</span></span>
<span data-ttu-id="a39c6-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a39c6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a39c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39c6-120">-DefaultProfile</span></span>
<span data-ttu-id="a39c6-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a39c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39c6-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a39c6-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="a39c6-123">Az Internet biztonságának engedélyezése ehhez a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="a39c6-123">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="a39c6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a39c6-124">-Name</span></span>
<span data-ttu-id="a39c6-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a39c6-125">The resource name.</span></span>

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

### <span data-ttu-id="a39c6-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a39c6-126">-ParentObject</span></span>
<span data-ttu-id="a39c6-127">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a39c6-127">The parent resource.</span></span>

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

### <span data-ttu-id="a39c6-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a39c6-128">-ParentResourceId</span></span>
<span data-ttu-id="a39c6-129">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a39c6-129">The parent resource.</span></span>

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

### <span data-ttu-id="a39c6-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a39c6-130">-ParentResourceName</span></span>
<span data-ttu-id="a39c6-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a39c6-131">The resource group name.</span></span>

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

### <span data-ttu-id="a39c6-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a39c6-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="a39c6-133">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="a39c6-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="a39c6-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a39c6-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="a39c6-135">Az a távoli virtuális hálózat, amelyre a hub virtuális hálózati kapcsolata van csatlakoztatva.</span><span class="sxs-lookup"><span data-stu-id="a39c6-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="a39c6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39c6-136">-ResourceGroupName</span></span>
<span data-ttu-id="a39c6-137">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a39c6-137">The resource group name.</span></span>

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

### <span data-ttu-id="a39c6-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a39c6-138">-Confirm</span></span>
<span data-ttu-id="a39c6-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a39c6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39c6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39c6-140">-WhatIf</span></span>
<span data-ttu-id="a39c6-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a39c6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39c6-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a39c6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39c6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39c6-143">CommonParameters</span></span>
<span data-ttu-id="a39c6-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a39c6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39c6-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a39c6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39c6-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a39c6-146">INPUTS</span></span>

### <span data-ttu-id="a39c6-147">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a39c6-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a39c6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a39c6-148">System.String</span></span>

## <span data-ttu-id="a39c6-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a39c6-149">OUTPUTS</span></span>

### <span data-ttu-id="a39c6-150">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="a39c6-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="a39c6-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a39c6-151">NOTES</span></span>

## <span data-ttu-id="a39c6-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a39c6-152">RELATED LINKS</span></span>

[<span data-ttu-id="a39c6-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a39c6-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="a39c6-154">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="a39c6-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
