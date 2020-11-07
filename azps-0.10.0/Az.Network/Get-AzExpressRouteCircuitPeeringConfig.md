---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841654"
---
# <span data-ttu-id="6da83-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6da83-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="6da83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6da83-102">SYNOPSIS</span></span>
<span data-ttu-id="6da83-103">ExpressRoute-áramköri peer-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="6da83-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="6da83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6da83-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da83-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6da83-105">DESCRIPTION</span></span>
<span data-ttu-id="6da83-106">A **Get-AzExpressRouteCircuitPeeringConfig** parancsmag kikeresi a ExpressRoute-áramkör kapcsolati viszonyának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="6da83-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6da83-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6da83-107">EXAMPLES</span></span>

### <span data-ttu-id="6da83-108">Példa 1: egy ExpressRoute-áramkör társközi konfigurációjának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="6da83-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="6da83-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6da83-109">PARAMETERS</span></span>

### <span data-ttu-id="6da83-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da83-110">-DefaultProfile</span></span>
<span data-ttu-id="6da83-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6da83-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da83-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6da83-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6da83-113">A társközi konfigurációt tartalmazó ExpressRoute Circuit objektum.</span><span class="sxs-lookup"><span data-stu-id="6da83-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="6da83-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6da83-114">-Name</span></span>
<span data-ttu-id="6da83-115">A beolvasni kívánt társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="6da83-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="6da83-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da83-116">CommonParameters</span></span>
<span data-ttu-id="6da83-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6da83-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da83-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da83-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da83-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6da83-119">INPUTS</span></span>

### <span data-ttu-id="6da83-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6da83-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="6da83-121">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6da83-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="6da83-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6da83-122">OUTPUTS</span></span>

### <span data-ttu-id="6da83-123">Microsoft. Azure. commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="6da83-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="6da83-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6da83-124">NOTES</span></span>

## <span data-ttu-id="6da83-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6da83-125">RELATED LINKS</span></span>

[<span data-ttu-id="6da83-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6da83-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="6da83-127">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6da83-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="6da83-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="6da83-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="6da83-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6da83-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
