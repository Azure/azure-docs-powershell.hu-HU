---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847457"
---
# <span data-ttu-id="bb053-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bb053-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="bb053-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb053-102">SYNOPSIS</span></span>
<span data-ttu-id="bb053-103">Frissít egy meglévő HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="bb053-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="bb053-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb053-104">SYNTAX</span></span>

### <span data-ttu-id="bb053-105">ByHubVirtualNetworkConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb053-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb053-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="bb053-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb053-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="bb053-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb053-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb053-108">DESCRIPTION</span></span>
<span data-ttu-id="bb053-109">Frissít egy meglévő HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="bb053-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="bb053-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bb053-110">EXAMPLES</span></span>

### <span data-ttu-id="bb053-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb053-111">Example 1</span></span>
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
```

<span data-ttu-id="bb053-112">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="bb053-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="bb053-113">Virtuális hálózati kapcsolat jön létre, amely a virtuális központhoz tartozó virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="bb053-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="bb053-114">Ez a virtuális hálózati kapcsolat az internetes biztonság engedélyezését követően frissül.</span><span class="sxs-lookup"><span data-stu-id="bb053-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="bb053-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb053-115">PARAMETERS</span></span>

### <span data-ttu-id="bb053-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb053-116">-AsJob</span></span>
<span data-ttu-id="bb053-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bb053-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb053-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb053-118">-DefaultProfile</span></span>
<span data-ttu-id="bb053-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb053-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb053-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="bb053-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="bb053-121">Engedélyezze az internetes biztonságot ehhez a kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="bb053-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb053-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb053-122">-InputObject</span></span>
<span data-ttu-id="bb053-123">A módosítani kívánt hubvirtualnetworkconnection-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="bb053-123">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="bb053-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb053-124">-Name</span></span>
<span data-ttu-id="bb053-125">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bb053-125">The resource name.</span></span>

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

### <span data-ttu-id="bb053-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bb053-126">-ParentResourceName</span></span>
<span data-ttu-id="bb053-127">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bb053-127">The parent resource name.</span></span>

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

### <span data-ttu-id="bb053-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb053-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb053-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb053-129">The resource group name.</span></span>

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

### <span data-ttu-id="bb053-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb053-130">-ResourceId</span></span>
<span data-ttu-id="bb053-131">A módosítandó hubvirtualnetworkconnection erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bb053-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="bb053-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb053-132">-Confirm</span></span>
<span data-ttu-id="bb053-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb053-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb053-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb053-134">-WhatIf</span></span>
<span data-ttu-id="bb053-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb053-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb053-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb053-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb053-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb053-137">CommonParameters</span></span>
<span data-ttu-id="bb053-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb053-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb053-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb053-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb053-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb053-140">INPUTS</span></span>

### <span data-ttu-id="bb053-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bb053-141">System.String</span></span>

### <span data-ttu-id="bb053-142">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="bb053-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="bb053-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb053-143">OUTPUTS</span></span>

### <span data-ttu-id="bb053-144">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="bb053-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="bb053-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb053-145">NOTES</span></span>

## <span data-ttu-id="bb053-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb053-146">RELATED LINKS</span></span>