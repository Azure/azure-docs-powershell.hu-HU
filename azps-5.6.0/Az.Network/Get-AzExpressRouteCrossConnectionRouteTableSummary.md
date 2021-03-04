---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: d5b6d1b9e5d3955b7ecbff9dec02405e030bbf33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932410"
---
# <span data-ttu-id="fa492-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fa492-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="fa492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa492-102">SYNOPSIS</span></span>
<span data-ttu-id="fa492-103">Egy ExpressRoute-keresztkapcsolat útvonaltábláját összegző táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="fa492-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="fa492-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa492-104">SYNTAX</span></span>

### <span data-ttu-id="fa492-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="fa492-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa492-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="fa492-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa492-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa492-107">DESCRIPTION</span></span>
<span data-ttu-id="fa492-108">A **Get-AzExpressRouteCrossConnectionRouteTableSummary** parancsmag a BGP-szomszédos adatok összegzését olvassa be egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="fa492-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="fa492-109">Ezek az információk akkor hasznosak, ha meg szeretné határozni, hogy mennyi ideig jött létre az útválasztási környezet, és hogy hány útvonalelőtag van meghirdetve a társközi útválasztóban.</span><span class="sxs-lookup"><span data-stu-id="fa492-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="fa492-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa492-110">EXAMPLES</span></span>

### <span data-ttu-id="fa492-111">1. példa: Az elsődleges útvonal útvonal-összesítésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="fa492-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="fa492-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa492-112">PARAMETERS</span></span>

### <span data-ttu-id="fa492-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="fa492-113">-CrossConnectionName</span></span>
<span data-ttu-id="fa492-114">Az Express Route Cross Connection neve</span><span class="sxs-lookup"><span data-stu-id="fa492-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="fa492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa492-115">-DefaultProfile</span></span>
<span data-ttu-id="fa492-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa492-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa492-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="fa492-117">-DevicePath</span></span>
<span data-ttu-id="fa492-118">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="fa492-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="fa492-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fa492-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="fa492-120">The Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="fa492-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="fa492-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="fa492-121">-PeeringType</span></span>
<span data-ttu-id="fa492-122">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="fa492-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="fa492-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa492-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa492-124">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fa492-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="fa492-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa492-125">CommonParameters</span></span>
<span data-ttu-id="fa492-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa492-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa492-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa492-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa492-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa492-128">INPUTS</span></span>

### <span data-ttu-id="fa492-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fa492-129">None</span></span>
<span data-ttu-id="fa492-130">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="fa492-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa492-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa492-131">OUTPUTS</span></span>

### <span data-ttu-id="fa492-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="fa492-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="fa492-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa492-133">NOTES</span></span>

## <span data-ttu-id="fa492-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa492-134">RELATED LINKS</span></span>

[<span data-ttu-id="fa492-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="fa492-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="fa492-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa492-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
