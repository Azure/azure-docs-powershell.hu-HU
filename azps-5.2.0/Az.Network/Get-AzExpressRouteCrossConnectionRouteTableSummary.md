---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329741"
---
# <span data-ttu-id="542ee-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="542ee-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="542ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542ee-102">SYNOPSIS</span></span>
<span data-ttu-id="542ee-103">Egy ExpressRoute-keresztkapcsolat útvonaltábláját összegző táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="542ee-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="542ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="542ee-104">SYNTAX</span></span>

### <span data-ttu-id="542ee-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="542ee-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="542ee-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="542ee-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="542ee-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="542ee-107">DESCRIPTION</span></span>
<span data-ttu-id="542ee-108">A **Get-AzExpressRouteCrossConnectionRouteTableSummary** parancsmag a BGP-szomszédos adatok összegzését olvassa be egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="542ee-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="542ee-109">Ezek az információk akkor hasznosak, ha meg szeretné határozni, hogy mennyi ideig jött létre az útválasztási környezet, és hogy hány útvonalelőtag van meghirdetve a társközi útválasztóban.</span><span class="sxs-lookup"><span data-stu-id="542ee-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="542ee-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="542ee-110">EXAMPLES</span></span>

### <span data-ttu-id="542ee-111">1. példa: Az elsődleges útvonal útvonal-összesítésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="542ee-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="542ee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="542ee-112">PARAMETERS</span></span>

### <span data-ttu-id="542ee-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="542ee-113">-CrossConnectionName</span></span>
<span data-ttu-id="542ee-114">Az Express Route Cross Connection neve</span><span class="sxs-lookup"><span data-stu-id="542ee-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="542ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542ee-115">-DefaultProfile</span></span>
<span data-ttu-id="542ee-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="542ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="542ee-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="542ee-117">-DevicePath</span></span>
<span data-ttu-id="542ee-118">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="542ee-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="542ee-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="542ee-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="542ee-120">Az Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="542ee-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="542ee-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="542ee-121">-PeeringType</span></span>
<span data-ttu-id="542ee-122">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="542ee-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="542ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="542ee-124">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="542ee-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="542ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542ee-125">CommonParameters</span></span>
<span data-ttu-id="542ee-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542ee-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="542ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542ee-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="542ee-128">INPUTS</span></span>

### <span data-ttu-id="542ee-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="542ee-129">None</span></span>
<span data-ttu-id="542ee-130">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="542ee-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="542ee-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="542ee-131">OUTPUTS</span></span>

### <span data-ttu-id="542ee-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="542ee-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="542ee-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="542ee-133">NOTES</span></span>

## <span data-ttu-id="542ee-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="542ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="542ee-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="542ee-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="542ee-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="542ee-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
