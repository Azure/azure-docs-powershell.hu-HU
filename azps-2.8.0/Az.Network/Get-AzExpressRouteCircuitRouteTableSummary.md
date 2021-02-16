---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: bca0dde2947b214d13032b54681f2fc179c26af1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411535"
---
# <span data-ttu-id="3f00c-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3f00c-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="3f00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f00c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f00c-103">Egy ExpressRoute-kapcsolat kapcsolati kör útvonaltábláját összegző táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="3f00c-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3f00c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f00c-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f00c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f00c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f00c-106">A **Get-AzExpressRouteCircuitRouteTableSummary** parancsmag beolvassa a BGP-szomszédos adatok összegzését egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="3f00c-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="3f00c-107">Ezek az információk akkor hasznosak, ha meg szeretné határozni, hogy mennyi ideig jött létre az útválasztási környezet, és hogy hány útvonalelőtag van meghirdetve a társközi útválasztóban.</span><span class="sxs-lookup"><span data-stu-id="3f00c-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="3f00c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f00c-108">EXAMPLES</span></span>

### <span data-ttu-id="3f00c-109">1. példa: Az elsődleges útvonal útvonal-összesítésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="3f00c-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="3f00c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f00c-110">PARAMETERS</span></span>

### <span data-ttu-id="3f00c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f00c-111">-DefaultProfile</span></span>
<span data-ttu-id="3f00c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f00c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f00c-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="3f00c-113">-DevicePath</span></span>
<span data-ttu-id="3f00c-114">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="3f00c-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="3f00c-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="3f00c-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="3f00c-116">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="3f00c-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="3f00c-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3f00c-117">-PeeringType</span></span>
<span data-ttu-id="3f00c-118">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3f00c-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3f00c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f00c-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f00c-120">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f00c-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="3f00c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f00c-121">CommonParameters</span></span>
<span data-ttu-id="3f00c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f00c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f00c-123">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f00c-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f00c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f00c-124">INPUTS</span></span>

### <span data-ttu-id="3f00c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3f00c-125">System.String</span></span>

## <span data-ttu-id="3f00c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f00c-126">OUTPUTS</span></span>

### <span data-ttu-id="3f00c-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="3f00c-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="3f00c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f00c-128">NOTES</span></span>

## <span data-ttu-id="3f00c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f00c-129">RELATED LINKS</span></span>

[<span data-ttu-id="3f00c-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3f00c-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="3f00c-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f00c-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="3f00c-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="3f00c-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
