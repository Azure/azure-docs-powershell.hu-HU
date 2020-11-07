---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848805"
---
# <span data-ttu-id="e521c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e521c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e521c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e521c-102">SYNOPSIS</span></span>
<span data-ttu-id="e521c-103">ExpressRoute-áramköri peer-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="e521c-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e521c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e521c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e521c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e521c-105">DESCRIPTION</span></span>
<span data-ttu-id="e521c-106">A **Get-AzureRmExpressRouteCircuitPeeringConfig** parancsmag kikeresi a ExpressRoute-áramkör kapcsolati viszonyának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e521c-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e521c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e521c-107">EXAMPLES</span></span>

### <span data-ttu-id="e521c-108">Példa 1: egy ExpressRoute-áramkör társközi konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e521c-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="e521c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e521c-109">PARAMETERS</span></span>

### <span data-ttu-id="e521c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e521c-110">-DefaultProfile</span></span>
<span data-ttu-id="e521c-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e521c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e521c-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e521c-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e521c-113">A társközi konfigurációt tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="e521c-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e521c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e521c-114">-Name</span></span>
<span data-ttu-id="e521c-115">A beolvasni kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e521c-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e521c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e521c-116">CommonParameters</span></span>
<span data-ttu-id="e521c-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e521c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e521c-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e521c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e521c-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e521c-119">INPUTS</span></span>

### <span data-ttu-id="e521c-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e521c-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e521c-121">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e521c-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="e521c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e521c-122">OUTPUTS</span></span>

### <span data-ttu-id="e521c-123">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="e521c-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="e521c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e521c-124">NOTES</span></span>

## <span data-ttu-id="e521c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e521c-125">RELATED LINKS</span></span>

[<span data-ttu-id="e521c-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e521c-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e521c-127">Új – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e521c-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e521c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e521c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e521c-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e521c-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
