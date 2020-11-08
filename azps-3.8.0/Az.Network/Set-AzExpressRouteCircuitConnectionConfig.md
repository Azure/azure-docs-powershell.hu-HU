---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011346"
---
# <span data-ttu-id="bf122-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bf122-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="bf122-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf122-102">SYNOPSIS</span></span>
<span data-ttu-id="bf122-103">A privát kapcsolatokban létrehozott áramköri kapcsolat konfigurációjának frissítése az Express Route áramkörben.</span><span class="sxs-lookup"><span data-stu-id="bf122-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="bf122-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf122-104">SYNTAX</span></span>

### <span data-ttu-id="bf122-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf122-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf122-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf122-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf122-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf122-107">DESCRIPTION</span></span>
<span data-ttu-id="bf122-108">A **set-AzExpressRouteCircuitConnectionConfig** parancsmag egy ExpressRoute-áramkör személyes kinézetében létrehozott áramköri kapcsolati konfigurációt frissít.</span><span class="sxs-lookup"><span data-stu-id="bf122-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="bf122-109">Ez a beállítás lehetővé teszi a két útvonal közötti átirányítást régiónként vagy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="bf122-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="bf122-110">Fontos tudni, hogy a **set-AzExpressRouteCircuitConnectionConfig** futtatása előtt fel kell vennie az áramköri kapcsolatot a **Add-AzExpressRouteCircuitConnectionConfig** használatával.</span><span class="sxs-lookup"><span data-stu-id="bf122-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="bf122-111">A **set-AzExpressRouteCircuitPeeringConfig** futtatása után a Set-AzExpressRouteCircuit parancsmagot is el kell végeznie a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="bf122-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="bf122-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bf122-112">EXAMPLES</span></span>

### <span data-ttu-id="bf122-113">Példa 1: áramkör-kapcsolati erőforrás frissítése meglévő ExpressRoute-áramkörre</span><span class="sxs-lookup"><span data-stu-id="bf122-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="bf122-114">2. példa: az áramköri kapcsolat konfigurációjának beállítása csővezeték használatával meglévő ExpressRoute-áramkörrel</span><span class="sxs-lookup"><span data-stu-id="bf122-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="bf122-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf122-115">PARAMETERS</span></span>

### <span data-ttu-id="bf122-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bf122-116">-AddressPrefix</span></span>
<span data-ttu-id="bf122-117">Az IPv4-alagutak közötti VxLan-alagutak létrehozásához szükséges minimális/29 ügyféli címtartomány.</span><span class="sxs-lookup"><span data-stu-id="bf122-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="bf122-118">vagy legalább/125 ügyfél-címterület létrehozása az VxLan-alagutak között az IPv6-alagutak közötti útválasztási kapcsolatok között.</span><span class="sxs-lookup"><span data-stu-id="bf122-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="bf122-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="bf122-119">-AddressPrefixType</span></span>
<span data-ttu-id="bf122-120">Annak a címnek a címét adja meg, amelyhez a cím előtag tartozik.</span><span class="sxs-lookup"><span data-stu-id="bf122-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf122-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="bf122-121">-AuthorizationKey</span></span>
<span data-ttu-id="bf122-122">Meghatalmazási kulcs egy másik előfizetésben a társközi Express útvonal-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="bf122-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="bf122-123">A társközi áramkör engedélyezését meglévő parancsok segítségével lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="bf122-123">Authorization on peer circuit can be created using existing commands.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf122-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf122-124">-DefaultProfile</span></span>
<span data-ttu-id="bf122-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf122-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf122-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bf122-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bf122-127">A ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="bf122-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="bf122-128">Ez az Azure objektum a **Get-AzExpressRouteCircuit** parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="bf122-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf122-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf122-129">-Name</span></span>
<span data-ttu-id="bf122-130">A hozzáadni kívánt áramkör-kapcsolati erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bf122-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf122-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="bf122-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="bf122-132">Az erőforrás-azonosító a távoli áramkörről, amely az aktuális áramkörrel van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="bf122-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf122-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf122-133">-Confirm</span></span>
<span data-ttu-id="bf122-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf122-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf122-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf122-135">-WhatIf</span></span>
<span data-ttu-id="bf122-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf122-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf122-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf122-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf122-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf122-138">CommonParameters</span></span>
<span data-ttu-id="bf122-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf122-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf122-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf122-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf122-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf122-141">INPUTS</span></span>

### <span data-ttu-id="bf122-142">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bf122-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="bf122-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bf122-143">System.String</span></span>

## <span data-ttu-id="bf122-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf122-144">OUTPUTS</span></span>

### <span data-ttu-id="bf122-145">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bf122-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bf122-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf122-146">NOTES</span></span>

## <span data-ttu-id="bf122-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf122-147">RELATED LINKS</span></span>

[<span data-ttu-id="bf122-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bf122-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="bf122-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bf122-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="bf122-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="bf122-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="bf122-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bf122-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="bf122-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bf122-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
