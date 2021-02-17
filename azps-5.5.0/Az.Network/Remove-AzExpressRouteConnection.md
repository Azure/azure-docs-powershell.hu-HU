---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159003"
---
# <span data-ttu-id="728b6-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="728b6-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="728b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="728b6-102">SYNOPSIS</span></span>
<span data-ttu-id="728b6-103">Eltávolítja az ExpressRouteConnectiont.</span><span class="sxs-lookup"><span data-stu-id="728b6-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="728b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="728b6-104">SYNTAX</span></span>

### <span data-ttu-id="728b6-105">ByExpressRouteConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="728b6-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728b6-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="728b6-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="728b6-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="728b6-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728b6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="728b6-108">DESCRIPTION</span></span>
<span data-ttu-id="728b6-109">Eltávolítja az ExpressRouteConnectiont.</span><span class="sxs-lookup"><span data-stu-id="728b6-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="728b6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="728b6-110">EXAMPLES</span></span>

### <span data-ttu-id="728b6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="728b6-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="728b6-112">A fentiekkel létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure).</span><span class="sxs-lookup"><span data-stu-id="728b6-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="728b6-113">Ezután létrejön egy ExpressRoute-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="728b6-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="728b6-114">Miután létrehozta az átjárót, az ExpressRouteSite-hoz csatlakozik a New-AzExpressRouteConnection paranccsal.</span><span class="sxs-lookup"><span data-stu-id="728b6-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="728b6-115">Ezután eltávolítja a kapcsolatot a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="728b6-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="728b6-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="728b6-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="728b6-117">Ugyanaz, mint az 1. példa, de most eltávolítja a kapcsolatot a bevezető objektummal a Get-AzExpressRouteConnectionból.</span><span class="sxs-lookup"><span data-stu-id="728b6-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="728b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="728b6-118">PARAMETERS</span></span>

### <span data-ttu-id="728b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728b6-119">-DefaultProfile</span></span>
<span data-ttu-id="728b6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="728b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="728b6-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="728b6-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="728b6-122">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="728b6-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728b6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="728b6-123">-Force</span></span>
<span data-ttu-id="728b6-124">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="728b6-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="728b6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="728b6-125">-InputObject</span></span>
<span data-ttu-id="728b6-126">A frissítendve elérhető ExpressRouteConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="728b6-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="728b6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="728b6-127">-Name</span></span>
<span data-ttu-id="728b6-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="728b6-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728b6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="728b6-129">-PassThru</span></span>
<span data-ttu-id="728b6-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="728b6-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="728b6-131">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="728b6-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="728b6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728b6-132">-ResourceGroupName</span></span>
<span data-ttu-id="728b6-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="728b6-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728b6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="728b6-134">-ResourceId</span></span>
<span data-ttu-id="728b6-135">A törölni kívánt ExpressRouteConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="728b6-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728b6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="728b6-136">-Confirm</span></span>
<span data-ttu-id="728b6-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="728b6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728b6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728b6-138">-WhatIf</span></span>
<span data-ttu-id="728b6-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="728b6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728b6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="728b6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728b6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728b6-141">CommonParameters</span></span>
<span data-ttu-id="728b6-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728b6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728b6-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728b6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728b6-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="728b6-144">INPUTS</span></span>

### <span data-ttu-id="728b6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="728b6-145">System.String</span></span>

### <span data-ttu-id="728b6-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="728b6-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="728b6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="728b6-147">OUTPUTS</span></span>

### <span data-ttu-id="728b6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="728b6-148">System.Boolean</span></span>

## <span data-ttu-id="728b6-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="728b6-149">NOTES</span></span>

## <span data-ttu-id="728b6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="728b6-150">RELATED LINKS</span></span>
