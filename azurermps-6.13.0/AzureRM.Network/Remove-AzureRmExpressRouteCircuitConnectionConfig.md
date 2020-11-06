---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495021"
---
# <span data-ttu-id="350c7-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="350c7-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="350c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="350c7-102">SYNOPSIS</span></span>
<span data-ttu-id="350c7-103">ExpressRoute-áramköri kapcsolat konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="350c7-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="350c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="350c7-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="350c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="350c7-105">DESCRIPTION</span></span>
<span data-ttu-id="350c7-106">A **Remove-AzureRmExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az adott Express útvonal-áramkörrel társított ExpressRoute-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="350c7-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="350c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="350c7-107">EXAMPLES</span></span>

### <span data-ttu-id="350c7-108">Példa 1: áramkör-kapcsolati konfiguráció eltávolítása ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="350c7-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="350c7-109">2. példa: az áramköri kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="350c7-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="350c7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="350c7-110">PARAMETERS</span></span>

### <span data-ttu-id="350c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350c7-111">-DefaultProfile</span></span>
<span data-ttu-id="350c7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="350c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="350c7-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="350c7-114">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="350c7-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="350c7-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="350c7-115">-Name</span></span>
<span data-ttu-id="350c7-116">Az eltávolítandó áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="350c7-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="350c7-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="350c7-117">-Confirm</span></span>
<span data-ttu-id="350c7-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="350c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="350c7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350c7-119">-WhatIf</span></span>
<span data-ttu-id="350c7-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="350c7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="350c7-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="350c7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="350c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350c7-122">CommonParameters</span></span>
<span data-ttu-id="350c7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="350c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350c7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350c7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350c7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="350c7-125">INPUTS</span></span>

### <span data-ttu-id="350c7-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="350c7-127">Paraméterek: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="350c7-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="350c7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="350c7-128">OUTPUTS</span></span>

### <span data-ttu-id="350c7-129">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="350c7-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="350c7-130">NOTES</span></span>

## <span data-ttu-id="350c7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="350c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="350c7-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="350c7-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="350c7-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="350c7-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="350c7-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="350c7-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="350c7-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="350c7-136">Új – AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="350c7-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="350c7-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="350c7-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="350c7-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
