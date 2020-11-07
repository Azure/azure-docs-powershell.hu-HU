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
ms.locfileid: "93670181"
---
# <span data-ttu-id="f5da7-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5da7-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f5da7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5da7-102">SYNOPSIS</span></span>
<span data-ttu-id="f5da7-103">ExpressRoute-áramköri kapcsolat konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f5da7-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="f5da7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5da7-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5da7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5da7-105">DESCRIPTION</span></span>
<span data-ttu-id="f5da7-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az adott Express útvonal-áramkörrel társított ExpressRoute-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f5da7-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="f5da7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f5da7-107">EXAMPLES</span></span>

### <span data-ttu-id="f5da7-108">Példa 1: áramkör-kapcsolati konfiguráció eltávolítása ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="f5da7-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f5da7-109">2. példa: az áramköri kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="f5da7-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f5da7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5da7-110">PARAMETERS</span></span>

### <span data-ttu-id="f5da7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5da7-111">-DefaultProfile</span></span>
<span data-ttu-id="f5da7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5da7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5da7-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f5da7-114">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="f5da7-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f5da7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5da7-115">-Name</span></span>
<span data-ttu-id="f5da7-116">Az eltávolítandó áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="f5da7-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="f5da7-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5da7-117">-Confirm</span></span>
<span data-ttu-id="f5da7-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5da7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5da7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5da7-119">-WhatIf</span></span>
<span data-ttu-id="f5da7-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5da7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5da7-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5da7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5da7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5da7-122">CommonParameters</span></span>
<span data-ttu-id="f5da7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5da7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5da7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5da7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5da7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5da7-125">INPUTS</span></span>

### <span data-ttu-id="f5da7-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f5da7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5da7-127">OUTPUTS</span></span>

### <span data-ttu-id="f5da7-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f5da7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5da7-129">NOTES</span></span>

## <span data-ttu-id="f5da7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5da7-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5da7-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f5da7-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5da7-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f5da7-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5da7-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f5da7-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5da7-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f5da7-135">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f5da7-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f5da7-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f5da7-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f5da7-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)