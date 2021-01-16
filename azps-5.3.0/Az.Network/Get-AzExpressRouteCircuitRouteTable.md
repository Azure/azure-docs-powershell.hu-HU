---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466228"
---
# <span data-ttu-id="34592-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="34592-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="34592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34592-102">SYNOPSIS</span></span>
<span data-ttu-id="34592-103">Útvonaltáblát kap egy ExpressRoute-áramkörből.</span><span class="sxs-lookup"><span data-stu-id="34592-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="34592-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="34592-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34592-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="34592-105">DESCRIPTION</span></span>
<span data-ttu-id="34592-106">A **Get-AzExpressRouteCircuitRouteTable** parancsmag lekéri egy ExpressRoute-áramkör részletes útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="34592-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="34592-107">Az útvonaltábla az összes útvonalat mutatja, vagy szűrhető egy adott társviszony-típus útvonalának szűrésére.</span><span class="sxs-lookup"><span data-stu-id="34592-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="34592-108">Az útválasztási táblával ellenőrizheti a társviszony-konfigurációt és a csatlakozást.</span><span class="sxs-lookup"><span data-stu-id="34592-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="34592-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="34592-109">EXAMPLES</span></span>

### <span data-ttu-id="34592-110">1. példa: Az elsődleges útvonal útvonaltáblája</span><span class="sxs-lookup"><span data-stu-id="34592-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="34592-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34592-111">PARAMETERS</span></span>

### <span data-ttu-id="34592-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34592-112">-DefaultProfile</span></span>
<span data-ttu-id="34592-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34592-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34592-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="34592-114">-DevicePath</span></span>
<span data-ttu-id="34592-115">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="34592-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="34592-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="34592-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="34592-117">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="34592-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="34592-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="34592-118">-PeeringType</span></span>
<span data-ttu-id="34592-119">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="34592-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="34592-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34592-120">-ResourceGroupName</span></span>
<span data-ttu-id="34592-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="34592-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="34592-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34592-122">CommonParameters</span></span>
<span data-ttu-id="34592-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34592-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34592-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34592-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34592-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34592-125">INPUTS</span></span>

### <span data-ttu-id="34592-126">System.String</span><span class="sxs-lookup"><span data-stu-id="34592-126">System.String</span></span>

## <span data-ttu-id="34592-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34592-127">OUTPUTS</span></span>

### <span data-ttu-id="34592-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="34592-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="34592-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="34592-129">NOTES</span></span>

## <span data-ttu-id="34592-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34592-130">RELATED LINKS</span></span>

[<span data-ttu-id="34592-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="34592-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="34592-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="34592-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="34592-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="34592-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
