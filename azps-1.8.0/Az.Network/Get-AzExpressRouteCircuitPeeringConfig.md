---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670599"
---
# <span data-ttu-id="0c663-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c663-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0c663-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c663-102">SYNOPSIS</span></span>
<span data-ttu-id="0c663-103">ExpressRoute-áramköri peer-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="0c663-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0c663-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c663-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c663-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c663-105">DESCRIPTION</span></span>
<span data-ttu-id="0c663-106">A **Get-AzExpressRouteCircuitPeeringConfig** parancsmag kikeresi a ExpressRoute-áramkör kapcsolati viszonyának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0c663-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0c663-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0c663-107">EXAMPLES</span></span>

### <span data-ttu-id="0c663-108">Példa 1: egy ExpressRoute-áramkör társközi konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0c663-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="0c663-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c663-109">PARAMETERS</span></span>

### <span data-ttu-id="0c663-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c663-110">-DefaultProfile</span></span>
<span data-ttu-id="0c663-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c663-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c663-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c663-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0c663-113">A társközi konfigurációt tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="0c663-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="0c663-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c663-114">-Name</span></span>
<span data-ttu-id="0c663-115">A beolvasni kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="0c663-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="0c663-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c663-116">CommonParameters</span></span>
<span data-ttu-id="0c663-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c663-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c663-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0c663-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c663-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c663-119">INPUTS</span></span>

### <span data-ttu-id="0c663-120">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c663-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0c663-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c663-121">OUTPUTS</span></span>

### <span data-ttu-id="0c663-122">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="0c663-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="0c663-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c663-123">NOTES</span></span>

## <span data-ttu-id="0c663-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c663-124">RELATED LINKS</span></span>

[<span data-ttu-id="0c663-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c663-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0c663-126">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c663-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0c663-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c663-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0c663-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c663-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
