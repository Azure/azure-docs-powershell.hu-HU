---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 16a17ed437194963f3cfd715a6e5364c8f4348c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670113"
---
# <span data-ttu-id="cf883-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf883-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="cf883-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf883-102">SYNOPSIS</span></span>
<span data-ttu-id="cf883-103">A Remove-AzVirtualHubVnetConnection parancsmag eltávolítja azt az Azure virtuális hálózati kapcsolatot, amely távoli VNET hoz létre a központi VNET.</span><span class="sxs-lookup"><span data-stu-id="cf883-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="cf883-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf883-104">SYNTAX</span></span>

### <span data-ttu-id="cf883-105">ByHubVirtualNetworkConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf883-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf883-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="cf883-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf883-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="cf883-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf883-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf883-108">DESCRIPTION</span></span>
<span data-ttu-id="cf883-109">A Remove-AzVirtualHubVnetConnection parancsmag eltávolítja azt az Azure virtuális hálózati kapcsolatot, amely távoli VNET hoz létre a központi VNET.</span><span class="sxs-lookup"><span data-stu-id="cf883-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="cf883-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cf883-110">EXAMPLES</span></span>

### <span data-ttu-id="cf883-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf883-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="cf883-112">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="cf883-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="cf883-113">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="cf883-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="cf883-114">A hub virtuális hálózati kapcsolat létrehozása után eltávolítja a központi virtuális hálózati kapcsolatot az erőforráscsoport neve, a hub neve és a kapcsolat neve alapján.</span><span class="sxs-lookup"><span data-stu-id="cf883-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="cf883-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf883-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="cf883-116">A fentiekben létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub Közép-amerikai az Azure-beli erőforráscsoport területén.</span><span class="sxs-lookup"><span data-stu-id="cf883-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="cf883-117">Ezt követően virtuális hálózati kapcsolat jön létre, amely a virtuális hálózatot a virtuális központba fogja irányítani.</span><span class="sxs-lookup"><span data-stu-id="cf883-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="cf883-118">A hub virtuális hálózati kapcsolat létrehozása után eltávolítja a hub virtuális hálózati kapcsolatát PowerShell-csövekkel a kimenetről a Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="cf883-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="cf883-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf883-119">PARAMETERS</span></span>

### <span data-ttu-id="cf883-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf883-120">-AsJob</span></span>
<span data-ttu-id="cf883-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cf883-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf883-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf883-122">-DefaultProfile</span></span>
<span data-ttu-id="cf883-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf883-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf883-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cf883-124">-Force</span></span>
<span data-ttu-id="cf883-125">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf883-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cf883-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf883-126">-InputObject</span></span>
<span data-ttu-id="cf883-127">A módosítani kívánt hubvirtualnetworkconnection-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="cf883-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf883-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf883-128">-Name</span></span>
<span data-ttu-id="cf883-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cf883-129">The resource name.</span></span>

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

### <span data-ttu-id="cf883-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="cf883-130">-ParentResourceName</span></span>
<span data-ttu-id="cf883-131">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cf883-131">The parent resource name.</span></span>

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

### <span data-ttu-id="cf883-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf883-132">-PassThru</span></span>
<span data-ttu-id="cf883-133">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cf883-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf883-134">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="cf883-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf883-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf883-135">-ResourceGroupName</span></span>
<span data-ttu-id="cf883-136">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cf883-136">The resource group name.</span></span>

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

### <span data-ttu-id="cf883-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf883-137">-ResourceId</span></span>
<span data-ttu-id="cf883-138">A módosítandó hubvirtualnetworkconnection erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf883-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="cf883-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf883-139">-Confirm</span></span>
<span data-ttu-id="cf883-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf883-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf883-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf883-141">-WhatIf</span></span>
<span data-ttu-id="cf883-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf883-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf883-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf883-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf883-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf883-144">CommonParameters</span></span>
<span data-ttu-id="cf883-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf883-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf883-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf883-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf883-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf883-147">INPUTS</span></span>

### <span data-ttu-id="cf883-148">Microsoft. Azure. commands. Network. models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="cf883-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="cf883-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cf883-149">System.String</span></span>

## <span data-ttu-id="cf883-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf883-150">OUTPUTS</span></span>

### <span data-ttu-id="cf883-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf883-151">System.Boolean</span></span>

## <span data-ttu-id="cf883-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf883-152">NOTES</span></span>

## <span data-ttu-id="cf883-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf883-153">RELATED LINKS</span></span>

[<span data-ttu-id="cf883-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf883-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="cf883-155">Új – AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cf883-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
