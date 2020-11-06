---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 36cf08aa4cb201beac284ae2296dfa508bf4edba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493731"
---
# <span data-ttu-id="e837f-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e837f-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e837f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e837f-102">SYNOPSIS</span></span>
<span data-ttu-id="e837f-103">Eltávolít egy ExpressRoute-áramkör-összevonási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e837f-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e837f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e837f-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e837f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e837f-105">DESCRIPTION</span></span>
<span data-ttu-id="e837f-106">A **Remove-AzureRmExpressRouteCircuitPeeringConfig** parancsmag eltávolítja a ExpressRoute-áramköri kapcsolatok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="e837f-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="e837f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e837f-107">EXAMPLES</span></span>

### <span data-ttu-id="e837f-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="e837f-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="e837f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e837f-109">PARAMETERS</span></span>

### <span data-ttu-id="e837f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e837f-110">-DefaultProfile</span></span>
<span data-ttu-id="e837f-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e837f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e837f-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e837f-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e837f-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="e837f-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e837f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e837f-114">-Name</span></span>
<span data-ttu-id="e837f-115">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="e837f-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e837f-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e837f-116">-PeerAddressType</span></span>
<span data-ttu-id="e837f-117">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="e837f-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e837f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e837f-118">CommonParameters</span></span>
<span data-ttu-id="e837f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e837f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e837f-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e837f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e837f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e837f-121">INPUTS</span></span>

### <span data-ttu-id="e837f-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e837f-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e837f-123">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e837f-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="e837f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e837f-124">OUTPUTS</span></span>

### <span data-ttu-id="e837f-125">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e837f-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e837f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e837f-126">NOTES</span></span>

## <span data-ttu-id="e837f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e837f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e837f-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e837f-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e837f-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e837f-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e837f-130">Új – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e837f-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e837f-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e837f-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
