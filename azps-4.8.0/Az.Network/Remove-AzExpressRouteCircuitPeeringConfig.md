---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184095"
---
# <span data-ttu-id="b9bb8-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b9bb8-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b9bb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bb8-103">Eltávolít egy ExpressRoute-áramkör-összevonási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="b9bb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9bb8-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9bb8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="b9bb8-106">A **Remove-AzExpressRouteCircuitPeeringConfig** parancsmag eltávolítja a ExpressRoute-áramköri kapcsolatok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="b9bb8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="b9bb8-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="b9bb8-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="b9bb8-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9bb8-109">PARAMETERS</span></span>

### <span data-ttu-id="b9bb8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bb8-110">-DefaultProfile</span></span>
<span data-ttu-id="b9bb8-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9bb8-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9bb8-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b9bb8-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="b9bb8-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b9bb8-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9bb8-114">-Name</span></span>
<span data-ttu-id="b9bb8-115">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="b9bb8-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b9bb8-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b9bb8-116">-PeerAddressType</span></span>
<span data-ttu-id="b9bb8-117">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="b9bb8-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="b9bb8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bb8-118">CommonParameters</span></span>
<span data-ttu-id="b9bb8-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9bb8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bb8-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9bb8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bb8-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9bb8-121">INPUTS</span></span>

### <span data-ttu-id="b9bb8-122">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9bb8-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b9bb8-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9bb8-123">OUTPUTS</span></span>

### <span data-ttu-id="b9bb8-124">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9bb8-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b9bb8-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9bb8-125">NOTES</span></span>

## <span data-ttu-id="b9bb8-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9bb8-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9bb8-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b9bb8-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b9bb8-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9bb8-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b9bb8-129">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b9bb8-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b9bb8-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b9bb8-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
