---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195352"
---
# <span data-ttu-id="0ee4e-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4e-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0ee4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee4e-103">ExpressRoute-áramköri kapcsolat konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="0ee4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ee4e-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ee4e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ee4e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee4e-106">A **Remove-AzExpressRouteCircuitConnectionConfig** parancsmag eltávolítja az adott Express útvonal-áramkörrel társított ExpressRoute-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="0ee4e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ee4e-107">EXAMPLES</span></span>

### <span data-ttu-id="0ee4e-108">Példa 1: áramkör-kapcsolati konfiguráció eltávolítása ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="0ee4e-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0ee4e-109">2. példa: az áramköri kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0ee4e-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="0ee4e-110">3. példa: az áramkör-kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről egy adott cím család számára</span><span class="sxs-lookup"><span data-stu-id="0ee4e-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0ee4e-111">Példa 4: az áramkör-kapcsolat konfigurációjának eltávolítása egy ExpressRoute-áramkörről egy adott cím család számára</span><span class="sxs-lookup"><span data-stu-id="0ee4e-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0ee4e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-112">PARAMETERS</span></span>

### <span data-ttu-id="0ee4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee4e-113">-DefaultProfile</span></span>
<span data-ttu-id="0ee4e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ee4e-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0ee4e-116">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="0ee4e-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0ee4e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ee4e-117">-Name</span></span>
<span data-ttu-id="0ee4e-118">Az eltávolítandó áramkör-kapcsolat konfigurációjának neve.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="0ee4e-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="0ee4e-119">-AddressPrefixType</span></span>
<span data-ttu-id="0ee4e-120">Annak a címnek a családját adja meg, amelyet el kell távolítani a konfigból.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="0ee4e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ee4e-121">-Confirm</span></span>
<span data-ttu-id="0ee4e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ee4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ee4e-123">-WhatIf</span></span>
<span data-ttu-id="0ee4e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ee4e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ee4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee4e-126">CommonParameters</span></span>
<span data-ttu-id="0ee4e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ee4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee4e-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee4e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee4e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-129">INPUTS</span></span>

### <span data-ttu-id="0ee4e-130">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0ee4e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-131">OUTPUTS</span></span>

### <span data-ttu-id="0ee4e-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0ee4e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ee4e-133">NOTES</span></span>

## <span data-ttu-id="0ee4e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0ee4e-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0ee4e-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4e-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0ee4e-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4e-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0ee4e-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4e-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0ee4e-139">Új – AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0ee4e-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0ee4e-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0ee4e-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ee4e-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)