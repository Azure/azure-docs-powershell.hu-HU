---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151971"
---
# <span data-ttu-id="367be-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367be-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="367be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="367be-102">SYNOPSIS</span></span>
<span data-ttu-id="367be-103">ExpressRoute-kapcsolati társviszony-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="367be-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="367be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="367be-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="367be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="367be-105">DESCRIPTION</span></span>
<span data-ttu-id="367be-106">A **Get-AzExpressRouteCircuitPeeringConfig** parancsmag beolvassa egy társviszony konfigurációját egy ExpressRoute-áramkörben.</span><span class="sxs-lookup"><span data-stu-id="367be-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="367be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="367be-107">EXAMPLES</span></span>

### <span data-ttu-id="367be-108">1. példa: Az ExpressRoute-áramkör társviszony-konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="367be-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="367be-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="367be-109">PARAMETERS</span></span>

### <span data-ttu-id="367be-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367be-110">-DefaultProfile</span></span>
<span data-ttu-id="367be-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="367be-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="367be-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367be-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="367be-113">A társviszony-konfigurációt tartalmazó ExpressRoute-áramkör-objektum.</span><span class="sxs-lookup"><span data-stu-id="367be-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="367be-114">-Name</span><span class="sxs-lookup"><span data-stu-id="367be-114">-Name</span></span>
<span data-ttu-id="367be-115">A visszakeresni szükséges társviszony-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="367be-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="367be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367be-116">CommonParameters</span></span>
<span data-ttu-id="367be-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367be-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="367be-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367be-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="367be-119">INPUTS</span></span>

### <span data-ttu-id="367be-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367be-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="367be-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="367be-121">OUTPUTS</span></span>

### <span data-ttu-id="367be-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="367be-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="367be-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="367be-123">NOTES</span></span>

## <span data-ttu-id="367be-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="367be-124">RELATED LINKS</span></span>

[<span data-ttu-id="367be-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367be-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367be-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367be-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367be-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367be-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367be-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367be-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
