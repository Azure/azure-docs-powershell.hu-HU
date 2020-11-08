---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194228"
---
# <span data-ttu-id="31aca-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="31aca-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="31aca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31aca-102">SYNOPSIS</span></span>
<span data-ttu-id="31aca-103">Eltávolít egy ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="31aca-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="31aca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31aca-104">SYNTAX</span></span>

### <span data-ttu-id="31aca-105">ByExpressRouteConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31aca-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31aca-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="31aca-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31aca-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="31aca-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31aca-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="31aca-108">DESCRIPTION</span></span>
<span data-ttu-id="31aca-109">Eltávolít egy ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="31aca-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="31aca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31aca-110">EXAMPLES</span></span>

### <span data-ttu-id="31aca-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="31aca-111">Example 1</span></span>
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

<span data-ttu-id="31aca-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="31aca-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="31aca-113">Ezt követően egy ExpressRoute átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="31aca-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="31aca-114">Miután létrehozta az átjárót, az a New-AzExpressRouteConnection parancs segítségével csatlakozik a ExpressRouteSite.</span><span class="sxs-lookup"><span data-stu-id="31aca-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="31aca-115">Ezután eltávolítja a kapcsolatot a kapcsolat nevével.</span><span class="sxs-lookup"><span data-stu-id="31aca-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="31aca-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="31aca-116">Example 2</span></span>

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

<span data-ttu-id="31aca-117">Ugyanaz, mint a példa 1, de most már eltávolítja a kapcsolatot a Get-AzExpressRouteConnection-től a vezetékes objektummal.</span><span class="sxs-lookup"><span data-stu-id="31aca-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="31aca-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31aca-118">PARAMETERS</span></span>

### <span data-ttu-id="31aca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aca-119">-DefaultProfile</span></span>
<span data-ttu-id="31aca-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31aca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31aca-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="31aca-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="31aca-122">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="31aca-122">The parent resource name.</span></span>

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

### <span data-ttu-id="31aca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="31aca-123">-Force</span></span>
<span data-ttu-id="31aca-124">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31aca-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="31aca-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31aca-125">-InputObject</span></span>
<span data-ttu-id="31aca-126">A frissítendő ExpressRouteConnection objektum.</span><span class="sxs-lookup"><span data-stu-id="31aca-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="31aca-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31aca-127">-Name</span></span>
<span data-ttu-id="31aca-128">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="31aca-128">The resource name.</span></span>

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

### <span data-ttu-id="31aca-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31aca-129">-PassThru</span></span>
<span data-ttu-id="31aca-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="31aca-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="31aca-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="31aca-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31aca-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31aca-132">-ResourceGroupName</span></span>
<span data-ttu-id="31aca-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="31aca-133">The resource group name.</span></span>

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

### <span data-ttu-id="31aca-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31aca-134">-ResourceId</span></span>
<span data-ttu-id="31aca-135">A törlendő ExpressRouteConnection-objektum erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="31aca-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="31aca-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31aca-136">-Confirm</span></span>
<span data-ttu-id="31aca-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31aca-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31aca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31aca-138">-WhatIf</span></span>
<span data-ttu-id="31aca-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31aca-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31aca-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31aca-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31aca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aca-141">CommonParameters</span></span>
<span data-ttu-id="31aca-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31aca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aca-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31aca-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aca-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31aca-144">INPUTS</span></span>

### <span data-ttu-id="31aca-145">System. String</span><span class="sxs-lookup"><span data-stu-id="31aca-145">System.String</span></span>

### <span data-ttu-id="31aca-146">Microsoft. Azure. commands. Network. models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="31aca-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="31aca-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31aca-147">OUTPUTS</span></span>

### <span data-ttu-id="31aca-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31aca-148">System.Boolean</span></span>

## <span data-ttu-id="31aca-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31aca-149">NOTES</span></span>

## <span data-ttu-id="31aca-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31aca-150">RELATED LINKS</span></span>