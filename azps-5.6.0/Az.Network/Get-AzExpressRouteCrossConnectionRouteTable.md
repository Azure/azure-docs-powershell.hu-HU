---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932417"
---
# <span data-ttu-id="0db21-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0db21-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="0db21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db21-102">SYNOPSIS</span></span>
<span data-ttu-id="0db21-103">Útvonaltáblát kap egy ExpressRoute-keresztkapcsolatból.</span><span class="sxs-lookup"><span data-stu-id="0db21-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0db21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0db21-104">SYNTAX</span></span>

### <span data-ttu-id="0db21-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="0db21-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0db21-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="0db21-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0db21-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0db21-107">DESCRIPTION</span></span>
<span data-ttu-id="0db21-108">A **Get-AzExpressRouteCrossConnectionRouteTable** parancsmag beolvassa egy ExpressRoute-áramkör részletes útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="0db21-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="0db21-109">Az útvonaltábla az összes útvonalat mutatja, vagy szűrhető egy adott társviszony-típus útvonalának szűrésére.</span><span class="sxs-lookup"><span data-stu-id="0db21-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="0db21-110">Az útválasztási táblával ellenőrizheti a társviszony-konfigurációt és a csatlakozást.</span><span class="sxs-lookup"><span data-stu-id="0db21-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="0db21-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0db21-111">EXAMPLES</span></span>

### <span data-ttu-id="0db21-112">1. példa: Az elsődleges útvonal útvonaltáblája</span><span class="sxs-lookup"><span data-stu-id="0db21-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="0db21-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0db21-113">PARAMETERS</span></span>

### <span data-ttu-id="0db21-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="0db21-114">-CrossConnectionName</span></span>
<span data-ttu-id="0db21-115">Az Express Route Cross Connection neve</span><span class="sxs-lookup"><span data-stu-id="0db21-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db21-116">-DefaultProfile</span></span>
<span data-ttu-id="0db21-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0db21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db21-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="0db21-118">-DevicePath</span></span>
<span data-ttu-id="0db21-119">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="0db21-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="0db21-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0db21-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0db21-121">The Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="0db21-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db21-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0db21-122">-PeeringType</span></span>
<span data-ttu-id="0db21-123">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0db21-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0db21-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db21-124">-ResourceGroupName</span></span>
<span data-ttu-id="0db21-125">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0db21-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db21-126">CommonParameters</span></span>
<span data-ttu-id="0db21-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db21-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0db21-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db21-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0db21-129">INPUTS</span></span>

### <span data-ttu-id="0db21-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="0db21-130">None</span></span>
<span data-ttu-id="0db21-131">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="0db21-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0db21-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0db21-132">OUTPUTS</span></span>

### <span data-ttu-id="0db21-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="0db21-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="0db21-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0db21-134">NOTES</span></span>

## <span data-ttu-id="0db21-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0db21-135">RELATED LINKS</span></span>

[<span data-ttu-id="0db21-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="0db21-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="0db21-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0db21-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
