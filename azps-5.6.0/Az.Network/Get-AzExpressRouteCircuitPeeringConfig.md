---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007782"
---
# <span data-ttu-id="0ab71-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab71-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0ab71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab71-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab71-103">ExpressRoute-kapcsolati társviszony-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="0ab71-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0ab71-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ab71-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab71-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ab71-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab71-106">A **Get-AzExpressRouteCircuitPeeringConfig parancsmag** beolvassa egy társviszony konfigurációját egy ExpressRoute-áramkörben.</span><span class="sxs-lookup"><span data-stu-id="0ab71-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0ab71-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ab71-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab71-108">1. példa: Az ExpressRoute-áramkör társviszony-konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0ab71-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="0ab71-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ab71-109">PARAMETERS</span></span>

### <span data-ttu-id="0ab71-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab71-110">-DefaultProfile</span></span>
<span data-ttu-id="0ab71-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ab71-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ab71-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ab71-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0ab71-113">A társviszony-konfigurációt tartalmazó ExpressRoute-áramkör-objektum.</span><span class="sxs-lookup"><span data-stu-id="0ab71-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="0ab71-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0ab71-114">-Name</span></span>
<span data-ttu-id="0ab71-115">A visszakeresni szükséges társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0ab71-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="0ab71-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab71-116">CommonParameters</span></span>
<span data-ttu-id="0ab71-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab71-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab71-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ab71-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab71-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ab71-119">INPUTS</span></span>

### <span data-ttu-id="0ab71-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ab71-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0ab71-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab71-121">OUTPUTS</span></span>

### <span data-ttu-id="0ab71-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="0ab71-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="0ab71-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ab71-123">NOTES</span></span>

## <span data-ttu-id="0ab71-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ab71-124">RELATED LINKS</span></span>

[<span data-ttu-id="0ab71-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab71-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0ab71-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab71-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0ab71-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0ab71-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0ab71-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0ab71-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
