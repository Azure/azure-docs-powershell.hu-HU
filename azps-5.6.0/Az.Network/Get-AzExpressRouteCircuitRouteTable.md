---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 28a61e18f01f550f1b1ffd924119da3323905ad1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941089"
---
# <span data-ttu-id="36b35-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="36b35-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="36b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b35-102">SYNOPSIS</span></span>
<span data-ttu-id="36b35-103">Útvonaltáblát kap egy ExpressRoute-áramkörből.</span><span class="sxs-lookup"><span data-stu-id="36b35-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="36b35-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36b35-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36b35-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36b35-105">DESCRIPTION</span></span>
<span data-ttu-id="36b35-106">A **Get-AzExpressRouteCircuitRouteTable** parancsmag lekéri egy ExpressRoute-áramkör részletes útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="36b35-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="36b35-107">Az útvonaltábla az összes útvonalat mutatja, vagy szűrhető egy adott társviszony-típus útvonalának szűrésére.</span><span class="sxs-lookup"><span data-stu-id="36b35-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="36b35-108">Az útválasztási táblával ellenőrizheti a társviszony-konfigurációt és a csatlakozást.</span><span class="sxs-lookup"><span data-stu-id="36b35-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="36b35-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36b35-109">EXAMPLES</span></span>

### <span data-ttu-id="36b35-110">1. példa: Az elsődleges útvonal útvonaltáblája</span><span class="sxs-lookup"><span data-stu-id="36b35-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="36b35-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b35-111">PARAMETERS</span></span>

### <span data-ttu-id="36b35-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b35-112">-DefaultProfile</span></span>
<span data-ttu-id="36b35-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36b35-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b35-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="36b35-114">-DevicePath</span></span>
<span data-ttu-id="36b35-115">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="36b35-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b35-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="36b35-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="36b35-117">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="36b35-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b35-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="36b35-118">-PeeringType</span></span>
<span data-ttu-id="36b35-119">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="36b35-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b35-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b35-120">-ResourceGroupName</span></span>
<span data-ttu-id="36b35-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="36b35-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b35-122">CommonParameters</span></span>
<span data-ttu-id="36b35-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b35-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36b35-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b35-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36b35-125">INPUTS</span></span>

### <span data-ttu-id="36b35-126">System.String</span><span class="sxs-lookup"><span data-stu-id="36b35-126">System.String</span></span>

## <span data-ttu-id="36b35-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36b35-127">OUTPUTS</span></span>

### <span data-ttu-id="36b35-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="36b35-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="36b35-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36b35-129">NOTES</span></span>

## <span data-ttu-id="36b35-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36b35-130">RELATED LINKS</span></span>

[<span data-ttu-id="36b35-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="36b35-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="36b35-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="36b35-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="36b35-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="36b35-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
