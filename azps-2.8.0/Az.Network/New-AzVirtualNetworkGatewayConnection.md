---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c25b311a4f99814c718ce825d61433d7c2fee192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837910"
---
# <span data-ttu-id="81cb2-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81cb2-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="81cb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="81cb2-103">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="81cb2-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="81cb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81cb2-104">SYNTAX</span></span>

### <span data-ttu-id="81cb2-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81cb2-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81cb2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81cb2-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] 
 [-AsJob] [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81cb2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81cb2-107">DESCRIPTION</span></span>
<span data-ttu-id="81cb2-108">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="81cb2-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="81cb2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81cb2-109">EXAMPLES</span></span>

### <span data-ttu-id="81cb2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81cb2-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="81cb2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81cb2-111">PARAMETERS</span></span>

### <span data-ttu-id="81cb2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81cb2-112">-AsJob</span></span>
<span data-ttu-id="81cb2-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81cb2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81cb2-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="81cb2-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="81cb2-115">-ConnectionProtocol</span></span>
<span data-ttu-id="81cb2-116">Átjáró kapcsolódási protokollja: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="81cb2-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="81cb2-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cb2-118">-DefaultProfile</span></span>
<span data-ttu-id="81cb2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81cb2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81cb2-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="81cb2-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="81cb2-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="81cb2-122">-Force</span></span>

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

### <span data-ttu-id="81cb2-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="81cb2-123">-IpsecPolicies</span></span>
<span data-ttu-id="81cb2-124">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="81cb2-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-125">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="81cb2-125">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="81cb2-126">A forgalom kiválasztó házirendjeinek listája.</span><span class="sxs-lookup"><span data-stu-id="81cb2-126">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-127">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="81cb2-127">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="81cb2-128">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81cb2-129">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-130">-Peer</span><span class="sxs-lookup"><span data-stu-id="81cb2-130">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-131">-PeerId</span><span class="sxs-lookup"><span data-stu-id="81cb2-131">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cb2-132">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="81cb2-133">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="81cb2-134">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="81cb2-135">-Tag</span></span>
<span data-ttu-id="81cb2-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="81cb2-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81cb2-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="81cb2-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-138">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="81cb2-138">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="81cb2-139">Házirend-alapú forgalom kiválasztók használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="81cb2-139">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-140">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="81cb2-140">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-141">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="81cb2-141">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81cb2-142">-Confirm</span></span>
<span data-ttu-id="81cb2-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81cb2-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81cb2-144">-WhatIf</span></span>
<span data-ttu-id="81cb2-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81cb2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81cb2-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81cb2-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cb2-147">CommonParameters</span></span>
<span data-ttu-id="81cb2-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81cb2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cb2-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cb2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cb2-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81cb2-150">INPUTS</span></span>

### <span data-ttu-id="81cb2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="81cb2-151">System.String</span></span>

### <span data-ttu-id="81cb2-152">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="81cb2-152">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="81cb2-153">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="81cb2-153">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="81cb2-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81cb2-154">System.Int32</span></span>

### <span data-ttu-id="81cb2-155">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="81cb2-155">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="81cb2-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81cb2-156">System.Boolean</span></span>

### <span data-ttu-id="81cb2-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81cb2-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81cb2-158">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="81cb2-158">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="81cb2-159">Microsoft. Azure. commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="81cb2-159">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="81cb2-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81cb2-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81cb2-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81cb2-161">OUTPUTS</span></span>

### <span data-ttu-id="81cb2-162">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81cb2-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="81cb2-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81cb2-163">NOTES</span></span>

## <span data-ttu-id="81cb2-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81cb2-164">RELATED LINKS</span></span>

[<span data-ttu-id="81cb2-165">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81cb2-165">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="81cb2-166">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81cb2-166">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="81cb2-167">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81cb2-167">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
