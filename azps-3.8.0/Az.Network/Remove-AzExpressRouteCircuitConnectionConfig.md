---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: b01e0ecb48a5a4c27fc79448ca0e4d71e820d292
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014068"
---
# <span data-ttu-id="90a77-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90a77-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="90a77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a77-102">SYNOPSIS</span></span>
<span data-ttu-id="90a77-103">ExpressRoute-áramköri kapcsolat konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="90a77-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="90a77-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a77-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a77-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a77-105">DESCRIPTION</span></span>
<span data-ttu-id="90a77-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az adott Express útvonal-áramkörrel társított ExpressRoute-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="90a77-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="90a77-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90a77-107">EXAMPLES</span></span>

### <span data-ttu-id="90a77-108">Példa 1: áramkör-kapcsolati konfiguráció eltávolítása ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="90a77-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="90a77-109">2. példa: az áramköri kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="90a77-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="90a77-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a77-110">PARAMETERS</span></span>

### <span data-ttu-id="90a77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a77-111">-DefaultProfile</span></span>
<span data-ttu-id="90a77-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90a77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a77-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="90a77-114">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="90a77-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="90a77-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90a77-115">-Name</span></span>
<span data-ttu-id="90a77-116">Az eltávolítandó áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="90a77-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="90a77-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90a77-117">-Confirm</span></span>
<span data-ttu-id="90a77-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90a77-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a77-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a77-119">-WhatIf</span></span>
<span data-ttu-id="90a77-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90a77-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90a77-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90a77-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a77-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a77-122">CommonParameters</span></span>
<span data-ttu-id="90a77-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a77-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a77-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a77-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a77-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a77-125">INPUTS</span></span>

### <span data-ttu-id="90a77-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="90a77-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a77-127">OUTPUTS</span></span>

### <span data-ttu-id="90a77-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="90a77-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a77-129">NOTES</span></span>

## <span data-ttu-id="90a77-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a77-130">RELATED LINKS</span></span>

[<span data-ttu-id="90a77-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="90a77-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90a77-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="90a77-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90a77-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="90a77-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90a77-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="90a77-135">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="90a77-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="90a77-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="90a77-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="90a77-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)