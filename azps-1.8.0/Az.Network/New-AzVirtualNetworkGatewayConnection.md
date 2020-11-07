---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670260"
---
# <span data-ttu-id="81407-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81407-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="81407-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81407-102">SYNOPSIS</span></span>
<span data-ttu-id="81407-103">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="81407-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="81407-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81407-104">SYNTAX</span></span>

### <span data-ttu-id="81407-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81407-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81407-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="81407-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81407-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="81407-107">DESCRIPTION</span></span>
<span data-ttu-id="81407-108">A virtuális hálózati átjáró és a helyszíni VPN-eszköz közötti helyközi VPN-kapcsolat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="81407-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="81407-109">Példák</span><span class="sxs-lookup"><span data-stu-id="81407-109">EXAMPLES</span></span>

### <span data-ttu-id="81407-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81407-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="81407-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81407-111">PARAMETERS</span></span>

### <span data-ttu-id="81407-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81407-112">-AsJob</span></span>
<span data-ttu-id="81407-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81407-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81407-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="81407-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="81407-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="81407-115">-ConnectionType</span></span>

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

### <span data-ttu-id="81407-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81407-116">-DefaultProfile</span></span>
<span data-ttu-id="81407-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81407-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81407-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="81407-118">-EnableBgp</span></span>

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

### <span data-ttu-id="81407-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="81407-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="81407-120">-Force</span><span class="sxs-lookup"><span data-stu-id="81407-120">-Force</span></span>

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

### <span data-ttu-id="81407-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="81407-121">-IpsecPolicies</span></span>
<span data-ttu-id="81407-122">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="81407-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="81407-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="81407-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="81407-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="81407-124">-Location</span></span>

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

### <span data-ttu-id="81407-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81407-125">-Name</span></span>

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

### <span data-ttu-id="81407-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="81407-126">-Peer</span></span>

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

### <span data-ttu-id="81407-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="81407-127">-PeerId</span></span>

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

### <span data-ttu-id="81407-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81407-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="81407-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="81407-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="81407-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="81407-130">-SharedKey</span></span>

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

### <span data-ttu-id="81407-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="81407-131">-Tag</span></span>
<span data-ttu-id="81407-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="81407-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81407-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="81407-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81407-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="81407-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="81407-135">Házirend-alapú forgalom kiválasztók használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="81407-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="81407-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="81407-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="81407-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="81407-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="81407-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81407-138">-Confirm</span></span>
<span data-ttu-id="81407-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81407-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81407-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81407-140">-WhatIf</span></span>
<span data-ttu-id="81407-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81407-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81407-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81407-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81407-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81407-143">CommonParameters</span></span>
<span data-ttu-id="81407-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81407-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81407-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81407-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81407-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81407-146">INPUTS</span></span>

### <span data-ttu-id="81407-147">System. String</span><span class="sxs-lookup"><span data-stu-id="81407-147">System.String</span></span>

### <span data-ttu-id="81407-148">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="81407-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="81407-149">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="81407-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="81407-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="81407-150">System.Int32</span></span>

### <span data-ttu-id="81407-151">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="81407-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="81407-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81407-152">System.Boolean</span></span>

### <span data-ttu-id="81407-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="81407-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="81407-154">Microsoft. Azure. commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="81407-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="81407-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81407-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81407-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81407-156">OUTPUTS</span></span>

### <span data-ttu-id="81407-157">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81407-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="81407-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81407-158">NOTES</span></span>

## <span data-ttu-id="81407-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81407-159">RELATED LINKS</span></span>

[<span data-ttu-id="81407-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81407-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="81407-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81407-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="81407-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="81407-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
