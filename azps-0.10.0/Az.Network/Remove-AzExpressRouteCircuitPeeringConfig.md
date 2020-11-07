---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841157"
---
# <span data-ttu-id="a6635-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a6635-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a6635-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6635-102">SYNOPSIS</span></span>
<span data-ttu-id="a6635-103">Eltávolít egy ExpressRoute-áramkör-összevonási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a6635-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a6635-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6635-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6635-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6635-105">DESCRIPTION</span></span>
<span data-ttu-id="a6635-106">A **Remove-AzExpressRouteCircuitPeeringConfig** parancsmag eltávolítja a ExpressRoute-áramköri kapcsolatok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a6635-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a6635-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6635-107">EXAMPLES</span></span>

### <span data-ttu-id="a6635-108">Példa 1: társközi konfiguráció eltávolítása egy ExpressRoute-áramkörről</span><span class="sxs-lookup"><span data-stu-id="a6635-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a6635-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6635-109">PARAMETERS</span></span>

### <span data-ttu-id="a6635-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6635-110">-DefaultProfile</span></span>
<span data-ttu-id="a6635-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6635-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6635-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6635-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a6635-113">Az eltávolítani kívánt társközi konfigurációt tartalmazó ExpressRoute-áramkör</span><span class="sxs-lookup"><span data-stu-id="a6635-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a6635-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6635-114">-Name</span></span>
<span data-ttu-id="a6635-115">Az eltávolítandó társközi konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="a6635-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a6635-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a6635-116">-PeerAddressType</span></span>
<span data-ttu-id="a6635-117">A társközi cím családja</span><span class="sxs-lookup"><span data-stu-id="a6635-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="a6635-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6635-118">CommonParameters</span></span>
<span data-ttu-id="a6635-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6635-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6635-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6635-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6635-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6635-121">INPUTS</span></span>

### <span data-ttu-id="a6635-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6635-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="a6635-123">A ' ExpressRouteCircuit ' paraméter az "PSExpressRouteCircuit" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a6635-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="a6635-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6635-124">OUTPUTS</span></span>

### <span data-ttu-id="a6635-125">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6635-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a6635-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6635-126">NOTES</span></span>

## <span data-ttu-id="a6635-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6635-127">RELATED LINKS</span></span>

[<span data-ttu-id="a6635-128">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a6635-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a6635-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6635-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a6635-130">Új – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a6635-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a6635-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a6635-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
