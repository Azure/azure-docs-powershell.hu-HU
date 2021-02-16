---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402133"
---
# <span data-ttu-id="907c3-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="907c3-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="907c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907c3-102">SYNOPSIS</span></span>
<span data-ttu-id="907c3-103">Kapcsolati konfigurációt ad az Express Route Circuit magánjellegű társviszony-létesítéshez.</span><span class="sxs-lookup"><span data-stu-id="907c3-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="907c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="907c3-104">SYNTAX</span></span>

### <span data-ttu-id="907c3-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="907c3-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907c3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="907c3-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907c3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="907c3-107">DESCRIPTION</span></span>
<span data-ttu-id="907c3-108">Az **Add-AzExpressRouteCircuitConnectionConfig** parancsmag kapcsolatkonfigurációt ad az ExpressRoute-áramkörök magánjellegű társviszony-létesítéshez.</span><span class="sxs-lookup"><span data-stu-id="907c3-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="907c3-109">Ez lehetővé teszi két Express Route Circuits régiók vagy előfizetések közötti társviszony-létesítését. Vegye figyelembe, hogy az **Add-AzExpressRouteCircuitPeeringConfig** futtatása után a Set-AzExpressRouteCircuit parancsmagot kell felhívnia a konfiguráció aktiválásához.</span><span class="sxs-lookup"><span data-stu-id="907c3-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="907c3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="907c3-110">EXAMPLES</span></span>

### <span data-ttu-id="907c3-111">1. példa: Kapcsolatcsoport-kapcsolati erőforrás hozzáadása meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="907c3-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="907c3-112">2. példa: Kapcsolati kapcsolat beállítása a Piping használatával egy meglévő ExpressRoute-áramkörhöz</span><span class="sxs-lookup"><span data-stu-id="907c3-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="907c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907c3-113">PARAMETERS</span></span>

### <span data-ttu-id="907c3-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="907c3-114">-AddressPrefix</span></span>
<span data-ttu-id="907c3-115">Legalább /29 ügyfélcímterület az Express Route Circuits VxLan-alagutak létrehozásához</span><span class="sxs-lookup"><span data-stu-id="907c3-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="907c3-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="907c3-116">-AuthorizationKey</span></span>
<span data-ttu-id="907c3-117">Engedélyezési kulcs társi Express Route Circuit-hez egy másik előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="907c3-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="907c3-118">A társ áramkörön az engedélyezés meglévő parancsokkal is létre lehet hozva.</span><span class="sxs-lookup"><span data-stu-id="907c3-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="907c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907c3-119">-DefaultProfile</span></span>
<span data-ttu-id="907c3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="907c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="907c3-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="907c3-122">Az ExpressRoute-áramkör módosul.</span><span class="sxs-lookup"><span data-stu-id="907c3-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="907c3-123">Ez a **Get-AzExpressRouteCircuit** parancsmag által visszaadott Azure-objektum.</span><span class="sxs-lookup"><span data-stu-id="907c3-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="907c3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="907c3-124">-Name</span></span>
<span data-ttu-id="907c3-125">A hozzáadni szükséges kapcsolatcsoport-kapcsolaterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="907c3-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="907c3-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="907c3-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="907c3-127">A távoli kapcsolatcsoport magánjellegű társviszony-létesítésének erőforrás-azonosítója, amelynek társviszonya az aktuális áramkörrel fog.</span><span class="sxs-lookup"><span data-stu-id="907c3-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="907c3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="907c3-128">-Confirm</span></span>
<span data-ttu-id="907c3-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="907c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907c3-130">-WhatIf</span></span>
<span data-ttu-id="907c3-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="907c3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="907c3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="907c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907c3-133">CommonParameters</span></span>
<span data-ttu-id="907c3-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907c3-135">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907c3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="907c3-136">INPUTS</span></span>

### <span data-ttu-id="907c3-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="907c3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="907c3-138">System.String</span></span>

## <span data-ttu-id="907c3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="907c3-139">OUTPUTS</span></span>

### <span data-ttu-id="907c3-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="907c3-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="907c3-141">NOTES</span></span>

## <span data-ttu-id="907c3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="907c3-142">RELATED LINKS</span></span>

[<span data-ttu-id="907c3-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="907c3-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="907c3-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="907c3-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="907c3-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="907c3-146">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="907c3-147">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="907c3-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
