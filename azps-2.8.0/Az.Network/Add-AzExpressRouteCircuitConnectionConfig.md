---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837683"
---
# <span data-ttu-id="0eee5-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0eee5-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0eee5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0eee5-102">SYNOPSIS</span></span>
<span data-ttu-id="0eee5-103">Áramkör-kapcsolati konfigurációt ad az Express Route-áramkör privát kinézetéhez.</span><span class="sxs-lookup"><span data-stu-id="0eee5-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="0eee5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0eee5-104">SYNTAX</span></span>

### <span data-ttu-id="0eee5-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0eee5-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0eee5-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eee5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0eee5-107">DESCRIPTION</span></span>
<span data-ttu-id="0eee5-108">Az **Add-AzExpressRouteCircuitConnectionConfig** parancsmag egy áramkör-kapcsolati konfigurációt ad egy ExpressRoute-áramkör személyes kinézetéhez.</span><span class="sxs-lookup"><span data-stu-id="0eee5-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="0eee5-109">Ez a beállítás lehetővé teszi a két útvonal közötti átirányítást régiónként vagy előfizetésben. Felhívjuk a figyelmét arra, hogy a **AzExpressRouteCircuitPeeringConfig** futtatása után az Set-AzExpressRouteCircuit parancsmagot kell hívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="0eee5-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="0eee5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0eee5-110">EXAMPLES</span></span>

### <span data-ttu-id="0eee5-111">1. példa: áramkör-kapcsolati erőforrás hozzáadása meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="0eee5-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0eee5-112">2. példa: áramkör-kapcsolati konfiguráció hozzáadása meglévő ExpressRoute-áramkörhöz csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0eee5-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0eee5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0eee5-113">PARAMETERS</span></span>

### <span data-ttu-id="0eee5-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0eee5-114">-AddressPrefix</span></span>
<span data-ttu-id="0eee5-115">Az VxLan-alagutak létrehozása az Express Route-áramkörök között minimális/29 ügyféli címtartomány segítségével</span><span class="sxs-lookup"><span data-stu-id="0eee5-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="0eee5-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0eee5-116">-AuthorizationKey</span></span>
<span data-ttu-id="0eee5-117">Meghatalmazási kulcs egy másik előfizetésben a társközi Express útvonal-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="0eee5-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="0eee5-118">A társközi áramkör engedélyezését meglévő parancsok segítségével lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="0eee5-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="0eee5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eee5-119">-DefaultProfile</span></span>
<span data-ttu-id="0eee5-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0eee5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eee5-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0eee5-122">A ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="0eee5-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="0eee5-123">Ez az Azure objektum a **Get-AzExpressRouteCircuit** parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="0eee5-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="0eee5-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0eee5-124">-Name</span></span>
<span data-ttu-id="0eee5-125">A hozzáadni kívánt áramkör-kapcsolati erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0eee5-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="0eee5-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="0eee5-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="0eee5-127">Az erőforrás-azonosító a távoli áramkörről, amely az aktuális áramkörrel van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="0eee5-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="0eee5-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0eee5-128">-Confirm</span></span>
<span data-ttu-id="0eee5-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0eee5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eee5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eee5-130">-WhatIf</span></span>
<span data-ttu-id="0eee5-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0eee5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eee5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0eee5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eee5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eee5-133">CommonParameters</span></span>
<span data-ttu-id="0eee5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0eee5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eee5-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eee5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eee5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eee5-136">INPUTS</span></span>

### <span data-ttu-id="0eee5-137">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="0eee5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0eee5-138">System.String</span></span>

## <span data-ttu-id="0eee5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eee5-139">OUTPUTS</span></span>

### <span data-ttu-id="0eee5-140">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0eee5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0eee5-141">NOTES</span></span>

## <span data-ttu-id="0eee5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eee5-142">RELATED LINKS</span></span>

[<span data-ttu-id="0eee5-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0eee5-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0eee5-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0eee5-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0eee5-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0eee5-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0eee5-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0eee5-147">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0eee5-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0eee5-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0eee5-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0eee5-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)