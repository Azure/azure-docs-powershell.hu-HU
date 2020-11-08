---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1f04b47889f334f095c8c3163bc601a3b1950c82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013280"
---
# <span data-ttu-id="ed084-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ed084-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="ed084-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed084-102">SYNOPSIS</span></span>
<span data-ttu-id="ed084-103">Virtuális hálózati kapcsolatot kap egy virtuális központban, vagy a virtuális hub minden virtuális hálózati kapcsolatát megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="ed084-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="ed084-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed084-104">SYNTAX</span></span>

### <span data-ttu-id="ed084-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed084-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed084-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ed084-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed084-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ed084-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed084-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed084-108">DESCRIPTION</span></span>
<span data-ttu-id="ed084-109">Virtuális hálózati kapcsolatot kap egy virtuális központban, vagy a virtuális hub minden virtuális hálózati kapcsolatát megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="ed084-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="ed084-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ed084-110">EXAMPLES</span></span>

### <span data-ttu-id="ed084-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed084-111">Example 1</span></span>
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
```

<span data-ttu-id="ed084-112">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="ed084-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="ed084-113">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="ed084-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="ed084-114">A hub virtuális hálózati kapcsolat létrehozása után a hub virtuális hálózati kapcsolata lesz az erőforráscsoport nevével, a hub nevével és a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="ed084-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="ed084-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed084-115">Example 2</span></span>

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
```

<span data-ttu-id="ed084-116">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="ed084-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="ed084-117">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="ed084-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="ed084-118">A hub virtuális hálózati kapcsolat létrehozása után az összes hub virtuális hálózati kapcsolat az erőforráscsoport nevével és a hub nevével jeleníthető meg.</span><span class="sxs-lookup"><span data-stu-id="ed084-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="ed084-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="ed084-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="ed084-120">Ez a parancsmag a hub virtuális hálózati kapcsolatait az erőforráscsoport nevével és a hub nevével kezdve jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ed084-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="ed084-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed084-121">PARAMETERS</span></span>

### <span data-ttu-id="ed084-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed084-122">-DefaultProfile</span></span>
<span data-ttu-id="ed084-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed084-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed084-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed084-124">-Name</span></span>
<span data-ttu-id="ed084-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ed084-125">The resource name.</span></span>

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

### <span data-ttu-id="ed084-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ed084-126">-ParentObject</span></span>
<span data-ttu-id="ed084-127">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ed084-127">The parent resource.</span></span>

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

### <span data-ttu-id="ed084-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ed084-128">-ParentResourceId</span></span>
<span data-ttu-id="ed084-129">A szülő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ed084-129">The parent resource id.</span></span>

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

### <span data-ttu-id="ed084-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ed084-130">-ParentResourceName</span></span>
<span data-ttu-id="ed084-131">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ed084-131">The parent resource name.</span></span>

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

### <span data-ttu-id="ed084-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed084-132">-ResourceGroupName</span></span>
<span data-ttu-id="ed084-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed084-133">The resource group name.</span></span>

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

### <span data-ttu-id="ed084-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed084-134">CommonParameters</span></span>
<span data-ttu-id="ed084-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed084-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed084-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed084-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed084-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed084-137">INPUTS</span></span>

### <span data-ttu-id="ed084-138">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ed084-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ed084-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ed084-139">System.String</span></span>

## <span data-ttu-id="ed084-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed084-140">OUTPUTS</span></span>

### <span data-ttu-id="ed084-141">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="ed084-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="ed084-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed084-142">NOTES</span></span>

## <span data-ttu-id="ed084-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed084-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed084-144">Új – AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ed084-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="ed084-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="ed084-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
