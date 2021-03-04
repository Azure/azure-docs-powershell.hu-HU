---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941674"
---
# <span data-ttu-id="29485-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="29485-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="29485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29485-102">SYNOPSIS</span></span>
<span data-ttu-id="29485-103">Eltávolít egy ExpressRoute-kapcsolati társviszony-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="29485-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="29485-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29485-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29485-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29485-105">DESCRIPTION</span></span>
<span data-ttu-id="29485-106">A **Remove-AzExpressRouteCircuitPeeringConfig** parancsmag eltávolítja az ExpressRoute-kapcsolat kapcsolati konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="29485-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="29485-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29485-107">EXAMPLES</span></span>

### <span data-ttu-id="29485-108">1. példa: Társviszony-konfiguráció eltávolítása ExpressRoute-áramkörből</span><span class="sxs-lookup"><span data-stu-id="29485-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="29485-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29485-109">PARAMETERS</span></span>

### <span data-ttu-id="29485-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29485-110">-DefaultProfile</span></span>
<span data-ttu-id="29485-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29485-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29485-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="29485-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="29485-113">Az eltávolítható társviszony-konfigurációt tartalmazó ExpressRoute-áramkör.</span><span class="sxs-lookup"><span data-stu-id="29485-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29485-114">-Name</span><span class="sxs-lookup"><span data-stu-id="29485-114">-Name</span></span>
<span data-ttu-id="29485-115">Az eltávolítható társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="29485-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="29485-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="29485-116">-PeerAddressType</span></span>
<span data-ttu-id="29485-117">A társviszony címjegyzéke</span><span class="sxs-lookup"><span data-stu-id="29485-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29485-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29485-118">CommonParameters</span></span>
<span data-ttu-id="29485-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29485-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29485-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29485-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29485-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29485-121">INPUTS</span></span>

### <span data-ttu-id="29485-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="29485-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="29485-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29485-123">OUTPUTS</span></span>

### <span data-ttu-id="29485-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="29485-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="29485-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29485-125">NOTES</span></span>

## <span data-ttu-id="29485-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29485-126">RELATED LINKS</span></span>

[<span data-ttu-id="29485-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="29485-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="29485-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="29485-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="29485-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="29485-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="29485-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="29485-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
