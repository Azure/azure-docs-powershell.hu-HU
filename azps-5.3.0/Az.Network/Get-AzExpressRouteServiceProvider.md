---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469289"
---
# <span data-ttu-id="b1135-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b1135-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b1135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1135-102">SYNOPSIS</span></span>
<span data-ttu-id="b1135-103">Listát kap az ExpressRoute-szolgáltatókról és jellemzőikről.</span><span class="sxs-lookup"><span data-stu-id="b1135-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="b1135-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1135-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1135-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1135-105">DESCRIPTION</span></span>
<span data-ttu-id="b1135-106">A **Get-AzExpressRouteServiceProvider parancsmag** beolvassa az ExpressRoute-szolgáltatók listáját és attribútumát.</span><span class="sxs-lookup"><span data-stu-id="b1135-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="b1135-107">Az attribútum tartalmazza a hely- és sávszélesség-beállításokat.</span><span class="sxs-lookup"><span data-stu-id="b1135-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="b1135-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1135-108">EXAMPLES</span></span>

### <span data-ttu-id="b1135-109">1. példa: A "Silicon Valley" szolgáltatásban található helyeket szolgáltatói lista lekérte</span><span class="sxs-lookup"><span data-stu-id="b1135-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="b1135-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1135-110">PARAMETERS</span></span>

### <span data-ttu-id="b1135-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1135-111">-DefaultProfile</span></span>
<span data-ttu-id="b1135-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1135-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1135-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1135-113">CommonParameters</span></span>
<span data-ttu-id="b1135-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1135-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1135-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1135-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1135-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1135-116">INPUTS</span></span>

### <span data-ttu-id="b1135-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1135-117">None</span></span>

## <span data-ttu-id="b1135-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1135-118">OUTPUTS</span></span>

### <span data-ttu-id="b1135-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b1135-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b1135-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1135-120">NOTES</span></span>

## <span data-ttu-id="b1135-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1135-121">RELATED LINKS</span></span>

[<span data-ttu-id="b1135-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b1135-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b1135-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1135-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b1135-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b1135-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b1135-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="b1135-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
