---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366882"
---
# <span data-ttu-id="88f2a-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="88f2a-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="88f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="88f2a-103">Eltávolítja az ExpressRoute-kapcsolat kapcsolatkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="88f2a-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="88f2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88f2a-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f2a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="88f2a-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az Adott ExpressRoute-kapcsolat kapcsolatkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="88f2a-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="88f2a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="88f2a-108">1. példa: Kapcsolati kapcsolat konfigurációjának eltávolítása ExpressRoute-áramkörből</span><span class="sxs-lookup"><span data-stu-id="88f2a-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="88f2a-109">2. példa: Áramköri kapcsolat konfigurációjának eltávolítása Egy ExpressRoute-áramkör pipázásával</span><span class="sxs-lookup"><span data-stu-id="88f2a-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="88f2a-110">3. példa: Kapcsolati kapcsolat konfigurációjának eltávolítása Egy adott cím családjához megadott ExpressRoute-áramkörből</span><span class="sxs-lookup"><span data-stu-id="88f2a-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="88f2a-111">4. példa: Áramköri kapcsolat konfigurációjának eltávolítása a Piping használatával egy ExpressRoute-áramkörből egy adott cím családjához</span><span class="sxs-lookup"><span data-stu-id="88f2a-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="88f2a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88f2a-112">PARAMETERS</span></span>

### <span data-ttu-id="88f2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f2a-113">-DefaultProfile</span></span>
<span data-ttu-id="88f2a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88f2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88f2a-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="88f2a-116">Az eltávolítható társviszony-konfigurációt tartalmazó ExpressRoute-áramkör.</span><span class="sxs-lookup"><span data-stu-id="88f2a-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="88f2a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="88f2a-117">-Name</span></span>
<span data-ttu-id="88f2a-118">Az eltávolítható kapcsolat kapcsolatkonfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="88f2a-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="88f2a-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="88f2a-119">-AddressPrefixType</span></span>
<span data-ttu-id="88f2a-120">Megadja, hogy a rendszer mely címeket távolítja el a konfigurációból.</span><span class="sxs-lookup"><span data-stu-id="88f2a-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f2a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88f2a-121">-Confirm</span></span>
<span data-ttu-id="88f2a-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="88f2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f2a-123">-WhatIf</span></span>
<span data-ttu-id="88f2a-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="88f2a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88f2a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88f2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f2a-126">CommonParameters</span></span>
<span data-ttu-id="88f2a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f2a-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f2a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f2a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88f2a-129">INPUTS</span></span>

### <span data-ttu-id="88f2a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="88f2a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88f2a-131">OUTPUTS</span></span>

### <span data-ttu-id="88f2a-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="88f2a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88f2a-133">NOTES</span></span>

## <span data-ttu-id="88f2a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88f2a-134">RELATED LINKS</span></span>

[<span data-ttu-id="88f2a-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="88f2a-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="88f2a-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="88f2a-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="88f2a-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="88f2a-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="88f2a-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="88f2a-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="88f2a-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="88f2a-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="88f2a-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88f2a-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)