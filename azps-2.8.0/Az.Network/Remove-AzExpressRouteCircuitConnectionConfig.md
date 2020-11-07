---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837114"
---
# <span data-ttu-id="3933a-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3933a-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="3933a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3933a-102">SYNOPSIS</span></span>
<span data-ttu-id="3933a-103">ExpressRoute-áramköri kapcsolat konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3933a-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="3933a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3933a-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3933a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3933a-105">DESCRIPTION</span></span>
<span data-ttu-id="3933a-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az adott Express útvonal-áramkörrel társított ExpressRoute-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3933a-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="3933a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3933a-107">EXAMPLES</span></span>

### <span data-ttu-id="3933a-108">Példa 1: áramkör-kapcsolati konfiguráció eltávolítása ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="3933a-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="3933a-109">2. példa: az áramköri kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="3933a-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="3933a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3933a-110">PARAMETERS</span></span>

### <span data-ttu-id="3933a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3933a-111">-DefaultProfile</span></span>
<span data-ttu-id="3933a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3933a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3933a-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3933a-114">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="3933a-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="3933a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3933a-115">-Name</span></span>
<span data-ttu-id="3933a-116">Az eltávolítandó áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="3933a-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="3933a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3933a-117">-Confirm</span></span>
<span data-ttu-id="3933a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3933a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3933a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3933a-119">-WhatIf</span></span>
<span data-ttu-id="3933a-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3933a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3933a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3933a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3933a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3933a-122">CommonParameters</span></span>
<span data-ttu-id="3933a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3933a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3933a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3933a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3933a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3933a-125">INPUTS</span></span>

### <span data-ttu-id="3933a-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3933a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3933a-127">OUTPUTS</span></span>

### <span data-ttu-id="3933a-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3933a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3933a-129">NOTES</span></span>

## <span data-ttu-id="3933a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3933a-130">RELATED LINKS</span></span>

[<span data-ttu-id="3933a-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3933a-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3933a-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3933a-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3933a-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3933a-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3933a-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3933a-135">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3933a-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3933a-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="3933a-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3933a-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)