---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160667"
---
# <span data-ttu-id="f3beb-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f3beb-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f3beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3beb-102">SYNOPSIS</span></span>
<span data-ttu-id="f3beb-103">A Remove-AzVirtualHubVnetConnection parancsmag eltávolít egy Azure Virtual Network-kapcsolatot, amely egy távoli VNET-kapcsolatot létesít a központi VNET-rel.</span><span class="sxs-lookup"><span data-stu-id="f3beb-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f3beb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3beb-104">SYNTAX</span></span>

### <span data-ttu-id="f3beb-105">ByHubVirtualNetworkConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3beb-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3beb-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f3beb-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3beb-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f3beb-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3beb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3beb-108">DESCRIPTION</span></span>
<span data-ttu-id="f3beb-109">A Remove-AzVirtualHubVnetConnection parancsmag eltávolít egy Azure Virtual Network-kapcsolatot, amely egy távoli VNET-kapcsolatot a központi VNET-nek társkod.</span><span class="sxs-lookup"><span data-stu-id="f3beb-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f3beb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3beb-110">EXAMPLES</span></span>

### <span data-ttu-id="f3beb-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3beb-111">Example 1</span></span>

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

<span data-ttu-id="f3beb-112">A fenti létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US) az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f3beb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f3beb-113">Ezután létrejön egy virtuális hálózati kapcsolat, amely a virtuális hálózat és a virtuális központ közötti társviszonyba fog hozni.</span><span class="sxs-lookup"><span data-stu-id="f3beb-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f3beb-114">Miután létrejött a központi virtuális hálózati kapcsolat, az erőforráscsoport nevét, a központ nevét és a kapcsolat nevét használva eltávolítja a központi virtuális hálózati kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="f3beb-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="f3beb-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="f3beb-115">Example 2</span></span>

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

<span data-ttu-id="f3beb-116">A fentiekkel az Azure-ban az adott erőforráscsoportban létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in Central US).</span><span class="sxs-lookup"><span data-stu-id="f3beb-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f3beb-117">Ezután létrejön egy virtuális hálózati kapcsolat, amely a virtuális hálózatot a virtuális központhoz társi kapcsolatban fogja létesíteni.</span><span class="sxs-lookup"><span data-stu-id="f3beb-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f3beb-118">Miután létrejött a központi virtuális hálózati kapcsolat, a get-AzHubVirtualNetworkConnection kimenetén powershell-piping használatával eltávolítja a központi virtuális hálózati kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="f3beb-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f3beb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3beb-119">PARAMETERS</span></span>

### <span data-ttu-id="f3beb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3beb-120">-AsJob</span></span>
<span data-ttu-id="f3beb-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f3beb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3beb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3beb-122">-DefaultProfile</span></span>
<span data-ttu-id="f3beb-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3beb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3beb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f3beb-124">-Force</span></span>
<span data-ttu-id="f3beb-125">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="f3beb-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3beb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3beb-126">-InputObject</span></span>
<span data-ttu-id="f3beb-127">A hubvirtualnetworkconnection resource to modify.</span><span class="sxs-lookup"><span data-stu-id="f3beb-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f3beb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f3beb-128">-Name</span></span>
<span data-ttu-id="f3beb-129">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f3beb-129">The resource name.</span></span>

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

### <span data-ttu-id="f3beb-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f3beb-130">-ParentResourceName</span></span>
<span data-ttu-id="f3beb-131">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f3beb-131">The parent resource name.</span></span>

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

### <span data-ttu-id="f3beb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3beb-132">-PassThru</span></span>
<span data-ttu-id="f3beb-133">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="f3beb-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3beb-134">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f3beb-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3beb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3beb-135">-ResourceGroupName</span></span>
<span data-ttu-id="f3beb-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3beb-136">The resource group name.</span></span>

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

### <span data-ttu-id="f3beb-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3beb-137">-ResourceId</span></span>
<span data-ttu-id="f3beb-138">A módosítani szükséges hubvirtualnetworkconnection erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f3beb-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="f3beb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3beb-139">-Confirm</span></span>
<span data-ttu-id="f3beb-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3beb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3beb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3beb-141">-WhatIf</span></span>
<span data-ttu-id="f3beb-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3beb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3beb-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3beb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3beb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3beb-144">CommonParameters</span></span>
<span data-ttu-id="f3beb-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3beb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3beb-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3beb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3beb-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3beb-147">INPUTS</span></span>

### <span data-ttu-id="f3beb-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f3beb-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="f3beb-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f3beb-149">System.String</span></span>

## <span data-ttu-id="f3beb-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3beb-150">OUTPUTS</span></span>

### <span data-ttu-id="f3beb-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3beb-151">System.Boolean</span></span>

## <span data-ttu-id="f3beb-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3beb-152">NOTES</span></span>

## <span data-ttu-id="f3beb-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3beb-153">RELATED LINKS</span></span>

[<span data-ttu-id="f3beb-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f3beb-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f3beb-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f3beb-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
