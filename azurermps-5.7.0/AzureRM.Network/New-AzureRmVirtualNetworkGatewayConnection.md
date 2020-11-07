---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5beb3e7c2c010570089dfd0667eca48e5d1c6728
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679283"
---
# <span data-ttu-id="b9e5e-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9e5e-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b9e5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9e5e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e5e-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9e5e-103">SYNTAX</span></span>

### <span data-ttu-id="b9e5e-104">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9e5e-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e5e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9e5e-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e5e-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9e5e-106">DESCRIPTION</span></span>

## <span data-ttu-id="b9e5e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e5e-108">1:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="b9e5e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9e5e-109">PARAMETERS</span></span>

### <span data-ttu-id="b9e5e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e5e-110">-AsJob</span></span>
<span data-ttu-id="b9e5e-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9e5e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e5e-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="b9e5e-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="b9e5e-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e5e-114">-DefaultProfile</span></span>
<span data-ttu-id="b9e5e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b9e5e-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b9e5e-117">-Force</span></span>
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

### <span data-ttu-id="b9e5e-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="b9e5e-118">-IpsecPolicies</span></span>
<span data-ttu-id="b9e5e-119">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-119">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="b9e5e-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="b9e5e-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9e5e-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="b9e5e-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="b9e5e-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e5e-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="b9e5e-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b9e5e-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="b9e5e-128">-Tag</span></span>
<span data-ttu-id="b9e5e-129">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b9e5e-130">Példa:</span><span class="sxs-lookup"><span data-stu-id="b9e5e-130">For example:</span></span>

<span data-ttu-id="b9e5e-131">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b9e5e-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b9e5e-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b9e5e-133">Házirend-alapú forgalom kiválasztók használata S2S-kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="b9e5e-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="b9e5e-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="b9e5e-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9e5e-136">-Confirm</span></span>
<span data-ttu-id="b9e5e-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e5e-138">-WhatIf</span></span>
<span data-ttu-id="b9e5e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e5e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e5e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e5e-141">CommonParameters</span></span>
<span data-ttu-id="b9e5e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9e5e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e5e-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e5e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e5e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e5e-144">INPUTS</span></span>

### <span data-ttu-id="b9e5e-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="b9e5e-145">None</span></span>
<span data-ttu-id="b9e5e-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b9e5e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9e5e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e5e-147">OUTPUTS</span></span>

### <span data-ttu-id="b9e5e-148">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9e5e-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b9e5e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9e5e-149">NOTES</span></span>

## <span data-ttu-id="b9e5e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9e5e-150">RELATED LINKS</span></span>

[<span data-ttu-id="b9e5e-151">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9e5e-151">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b9e5e-152">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9e5e-152">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b9e5e-153">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b9e5e-153">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
