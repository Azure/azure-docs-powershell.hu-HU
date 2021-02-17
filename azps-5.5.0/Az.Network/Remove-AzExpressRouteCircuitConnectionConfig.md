---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: fb82b00f998ed0c2b7473d4a3e0bcb9b3dc60630
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400025"
---
# <span data-ttu-id="1e351-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1e351-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="1e351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e351-102">SYNOPSIS</span></span>
<span data-ttu-id="1e351-103">Eltávolítja az ExpressRoute-kapcsolat kapcsolatkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1e351-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="1e351-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e351-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e351-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e351-105">DESCRIPTION</span></span>
<span data-ttu-id="1e351-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az Adott ExpressRoute-kapcsolat kapcsolatkonfigurációját.</span><span class="sxs-lookup"><span data-stu-id="1e351-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="1e351-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e351-107">EXAMPLES</span></span>

### <span data-ttu-id="1e351-108">1. példa: Kapcsolati kapcsolat konfigurációjának eltávolítása ExpressRoute-áramkörből</span><span class="sxs-lookup"><span data-stu-id="1e351-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="1e351-109">2. példa: Áramköri kapcsolat konfigurációjának eltávolítása Egy ExpressRoute-áramkör pipázásával</span><span class="sxs-lookup"><span data-stu-id="1e351-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="1e351-110">3. példa: Kapcsolat kapcsolati konfigurációjának eltávolítása egy ExpressRoute-áramkörből egy adott cím családjához</span><span class="sxs-lookup"><span data-stu-id="1e351-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="1e351-111">4. példa: Áramköri kapcsolat konfigurációjának eltávolítása a Piping használatával egy ExpressRoute-áramkörből egy adott cím családjához</span><span class="sxs-lookup"><span data-stu-id="1e351-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="1e351-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e351-112">PARAMETERS</span></span>

### <span data-ttu-id="1e351-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e351-113">-DefaultProfile</span></span>
<span data-ttu-id="1e351-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e351-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e351-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1e351-116">Az eltávolítható társviszony-konfigurációt tartalmazó ExpressRoute-áramkör.</span><span class="sxs-lookup"><span data-stu-id="1e351-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="1e351-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e351-117">-Name</span></span>
<span data-ttu-id="1e351-118">Az eltávolítható kapcsolat kapcsolatkonfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="1e351-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="1e351-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="1e351-119">-AddressPrefixType</span></span>
<span data-ttu-id="1e351-120">Megadja, hogy a rendszer mely címeket távolítja el a konfigurációból.</span><span class="sxs-lookup"><span data-stu-id="1e351-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="1e351-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e351-121">-Confirm</span></span>
<span data-ttu-id="1e351-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e351-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e351-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e351-123">-WhatIf</span></span>
<span data-ttu-id="1e351-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e351-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e351-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e351-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e351-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e351-126">CommonParameters</span></span>
<span data-ttu-id="1e351-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e351-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e351-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e351-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e351-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e351-129">INPUTS</span></span>

### <span data-ttu-id="1e351-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1e351-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e351-131">OUTPUTS</span></span>

### <span data-ttu-id="1e351-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1e351-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e351-133">NOTES</span></span>

## <span data-ttu-id="1e351-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e351-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e351-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1e351-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1e351-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="1e351-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1e351-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="1e351-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1e351-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)



[<span data-ttu-id="1e351-139">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-139">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="1e351-140">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e351-140">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
