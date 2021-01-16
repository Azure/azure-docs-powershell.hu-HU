---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466225"
---
# <span data-ttu-id="76155-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="76155-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="76155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76155-102">SYNOPSIS</span></span>
<span data-ttu-id="76155-103">Egy ExpressRoute-áramkör használati statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="76155-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="76155-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="76155-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76155-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="76155-105">DESCRIPTION</span></span>
<span data-ttu-id="76155-106">A **Get-AzExpressRouteCircuitStat** parancsmag beolvassa egy ExpressRoute-áramkör adatforgalmi statisztikáját.</span><span class="sxs-lookup"><span data-stu-id="76155-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="76155-107">A statisztikákban az elsődleges és a másodlagos útvonalon küldött és fogadott bájtok száma is szerepel.</span><span class="sxs-lookup"><span data-stu-id="76155-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="76155-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="76155-108">EXAMPLES</span></span>

### <span data-ttu-id="76155-109">1. példa: ExpressRoute-társ forgalmi statisztikáinak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="76155-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="76155-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76155-110">PARAMETERS</span></span>

### <span data-ttu-id="76155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76155-111">-DefaultProfile</span></span>
<span data-ttu-id="76155-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76155-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76155-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="76155-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="76155-114">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="76155-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="76155-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="76155-115">-PeeringType</span></span>
<span data-ttu-id="76155-116">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="76155-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76155-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76155-117">-ResourceGroupName</span></span>
<span data-ttu-id="76155-118">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="76155-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="76155-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76155-119">CommonParameters</span></span>
<span data-ttu-id="76155-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76155-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76155-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76155-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76155-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76155-122">INPUTS</span></span>

### <span data-ttu-id="76155-123">System.String</span><span class="sxs-lookup"><span data-stu-id="76155-123">System.String</span></span>

## <span data-ttu-id="76155-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76155-124">OUTPUTS</span></span>

### <span data-ttu-id="76155-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="76155-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="76155-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="76155-126">NOTES</span></span>

## <span data-ttu-id="76155-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76155-127">RELATED LINKS</span></span>

[<span data-ttu-id="76155-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="76155-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="76155-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="76155-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="76155-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="76155-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
