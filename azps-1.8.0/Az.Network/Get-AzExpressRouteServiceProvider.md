---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670569"
---
# <span data-ttu-id="b231d-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b231d-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b231d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b231d-102">SYNOPSIS</span></span>
<span data-ttu-id="b231d-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="b231d-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="b231d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b231d-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b231d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b231d-105">DESCRIPTION</span></span>
<span data-ttu-id="b231d-106">A **Get-AzExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="b231d-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="b231d-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b231d-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="b231d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b231d-108">EXAMPLES</span></span>

### <span data-ttu-id="b231d-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="b231d-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="b231d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b231d-110">PARAMETERS</span></span>

### <span data-ttu-id="b231d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b231d-111">-DefaultProfile</span></span>
<span data-ttu-id="b231d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b231d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b231d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b231d-113">CommonParameters</span></span>
<span data-ttu-id="b231d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b231d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b231d-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b231d-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b231d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b231d-116">INPUTS</span></span>

### <span data-ttu-id="b231d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="b231d-117">None</span></span>

## <span data-ttu-id="b231d-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b231d-118">OUTPUTS</span></span>

### <span data-ttu-id="b231d-119">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b231d-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b231d-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b231d-120">NOTES</span></span>

## <span data-ttu-id="b231d-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b231d-121">RELATED LINKS</span></span>

[<span data-ttu-id="b231d-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b231d-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b231d-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b231d-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b231d-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b231d-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b231d-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="b231d-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
