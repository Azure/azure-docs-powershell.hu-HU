---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025166"
---
# <span data-ttu-id="014cf-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="014cf-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="014cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="014cf-102">SYNOPSIS</span></span>
<span data-ttu-id="014cf-103">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="014cf-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="014cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="014cf-104">SYNTAX</span></span>

### <span data-ttu-id="014cf-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="014cf-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="014cf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="014cf-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="014cf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="014cf-107">DESCRIPTION</span></span>
<span data-ttu-id="014cf-108">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="014cf-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="014cf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="014cf-109">EXAMPLES</span></span>

### <span data-ttu-id="014cf-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="014cf-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="014cf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="014cf-111">PARAMETERS</span></span>

### <span data-ttu-id="014cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="014cf-112">-AsJob</span></span>
<span data-ttu-id="014cf-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="014cf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="014cf-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="014cf-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="014cf-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="014cf-115">-ConnectionProtocol</span></span>
<span data-ttu-id="014cf-116">Átjáró kapcsolódási protokollja: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="014cf-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="014cf-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="014cf-117">-ConnectionType</span></span>

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

### <span data-ttu-id="014cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014cf-118">-DefaultProfile</span></span>
<span data-ttu-id="014cf-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="014cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="014cf-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="014cf-120">-EnableBgp</span></span>

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

### <span data-ttu-id="014cf-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="014cf-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="014cf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="014cf-122">-Force</span></span>

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

### <span data-ttu-id="014cf-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="014cf-123">-IpsecPolicies</span></span>
<span data-ttu-id="014cf-124">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="014cf-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="014cf-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="014cf-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="014cf-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="014cf-126">-Location</span></span>

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

### <span data-ttu-id="014cf-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="014cf-127">-Name</span></span>

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

### <span data-ttu-id="014cf-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="014cf-128">-Peer</span></span>

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

### <span data-ttu-id="014cf-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="014cf-129">-PeerId</span></span>

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

### <span data-ttu-id="014cf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014cf-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="014cf-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="014cf-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="014cf-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="014cf-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="014cf-133">A kapcsolat elhalt-észlelési időtúllépése másodpercben</span><span class="sxs-lookup"><span data-stu-id="014cf-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="014cf-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="014cf-134">-SharedKey</span></span>

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

### <span data-ttu-id="014cf-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="014cf-135">-Tag</span></span>
<span data-ttu-id="014cf-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="014cf-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="014cf-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="014cf-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="014cf-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="014cf-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="014cf-139">A forgalom kiválasztó házirendjeinek listája.</span><span class="sxs-lookup"><span data-stu-id="014cf-139">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="014cf-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="014cf-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="014cf-141">Szeretné-e használni a PrivateIP-t ehhez a S2S VPN-alagúthoz</span><span class="sxs-lookup"><span data-stu-id="014cf-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="014cf-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="014cf-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="014cf-143">Házirend-alapú forgalom kiválasztók használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="014cf-143">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="014cf-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="014cf-144">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="014cf-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="014cf-145">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="014cf-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="014cf-146">-Confirm</span></span>
<span data-ttu-id="014cf-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="014cf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014cf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014cf-148">-WhatIf</span></span>
<span data-ttu-id="014cf-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="014cf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014cf-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="014cf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014cf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014cf-151">CommonParameters</span></span>
<span data-ttu-id="014cf-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="014cf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014cf-153">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="014cf-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014cf-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="014cf-154">INPUTS</span></span>

### <span data-ttu-id="014cf-155">System. String</span><span class="sxs-lookup"><span data-stu-id="014cf-155">System.String</span></span>

### <span data-ttu-id="014cf-156">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="014cf-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="014cf-157">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="014cf-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="014cf-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="014cf-158">System.Int32</span></span>

### <span data-ttu-id="014cf-159">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="014cf-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="014cf-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="014cf-160">System.Boolean</span></span>

### <span data-ttu-id="014cf-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="014cf-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="014cf-162">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="014cf-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="014cf-163">Microsoft. Azure. commands. Network. models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="014cf-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="014cf-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="014cf-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="014cf-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="014cf-165">OUTPUTS</span></span>

### <span data-ttu-id="014cf-166">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="014cf-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="014cf-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="014cf-167">NOTES</span></span>

## <span data-ttu-id="014cf-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="014cf-168">RELATED LINKS</span></span>

[<span data-ttu-id="014cf-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="014cf-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="014cf-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="014cf-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="014cf-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="014cf-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
