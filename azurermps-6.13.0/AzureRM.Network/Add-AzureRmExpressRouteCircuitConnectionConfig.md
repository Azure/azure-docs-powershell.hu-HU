---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503572"
---
# <span data-ttu-id="39515-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39515-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="39515-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39515-102">SYNOPSIS</span></span>
<span data-ttu-id="39515-103">Áramkör-kapcsolati konfigurációt ad az Express Route-áramkör privát kinézetéhez.</span><span class="sxs-lookup"><span data-stu-id="39515-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39515-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39515-104">SYNTAX</span></span>

### <span data-ttu-id="39515-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39515-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39515-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39515-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39515-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39515-107">DESCRIPTION</span></span>
<span data-ttu-id="39515-108">Az **Add-AzureRmExpressRouteCircuitConnectionConfig** parancsmag egy áramkör-kapcsolati konfigurációt ad egy ExpressRoute-áramkör személyes kinézetéhez.</span><span class="sxs-lookup"><span data-stu-id="39515-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="39515-109">Ez a beállítás lehetővé teszi a két útvonal közötti átirányítást régiónként vagy előfizetésben. Felhívjuk a figyelmét arra, hogy a **AzureRmExpressRouteCircuitPeeringConfig** futtatása után az Set-AzureRmExpressRouteCircuit parancsmagot kell hívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="39515-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="39515-110">Példák</span><span class="sxs-lookup"><span data-stu-id="39515-110">EXAMPLES</span></span>

### <span data-ttu-id="39515-111">1. példa: áramkör-kapcsolati erőforrás hozzáadása meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="39515-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="39515-112">2. példa: áramkör-kapcsolati konfiguráció hozzáadása meglévő ExpressRoute-áramkörhöz csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="39515-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="39515-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39515-113">PARAMETERS</span></span>

### <span data-ttu-id="39515-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="39515-114">-AddressPrefix</span></span>
<span data-ttu-id="39515-115">Az VxLan-alagutak létrehozása az Express Route-áramkörök között minimális/29 ügyféli címtartomány segítségével</span><span class="sxs-lookup"><span data-stu-id="39515-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="39515-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="39515-116">-AuthorizationKey</span></span>
<span data-ttu-id="39515-117">Meghatalmazási kulcs egy másik előfizetésben a társközi Express útvonal-áramkörhöz.</span><span class="sxs-lookup"><span data-stu-id="39515-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="39515-118">A társközi áramkör engedélyezését meglévő parancsok segítségével lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="39515-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="39515-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39515-119">-DefaultProfile</span></span>
<span data-ttu-id="39515-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39515-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39515-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="39515-122">A ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="39515-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="39515-123">Ez az Azure objektum a **Get-AzureRmExpressRouteCircuit** parancsmag által visszaadott érték.</span><span class="sxs-lookup"><span data-stu-id="39515-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="39515-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39515-124">-Name</span></span>
<span data-ttu-id="39515-125">A hozzáadni kívánt áramkör-kapcsolati erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="39515-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="39515-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="39515-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="39515-127">Az erőforrás-azonosító a távoli áramkörről, amely az aktuális áramkörrel van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="39515-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="39515-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39515-128">-Confirm</span></span>
<span data-ttu-id="39515-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39515-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39515-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39515-130">-WhatIf</span></span>
<span data-ttu-id="39515-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39515-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39515-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39515-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39515-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39515-133">CommonParameters</span></span>
<span data-ttu-id="39515-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39515-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39515-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39515-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39515-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39515-136">INPUTS</span></span>

### <span data-ttu-id="39515-137">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="39515-138">Paraméterek: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39515-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="39515-139">System. String</span><span class="sxs-lookup"><span data-stu-id="39515-139">System.String</span></span>

## <span data-ttu-id="39515-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39515-140">OUTPUTS</span></span>

### <span data-ttu-id="39515-141">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="39515-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39515-142">NOTES</span></span>

## <span data-ttu-id="39515-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39515-143">RELATED LINKS</span></span>

[<span data-ttu-id="39515-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="39515-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39515-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39515-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39515-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39515-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39515-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39515-148">Új – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="39515-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="39515-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="39515-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39515-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
