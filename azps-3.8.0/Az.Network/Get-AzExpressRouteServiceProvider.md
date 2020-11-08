---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 639e438a2ff3eb63282ba4f79aa984581128a082
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013352"
---
# <span data-ttu-id="03b86-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="03b86-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="03b86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03b86-102">SYNOPSIS</span></span>
<span data-ttu-id="03b86-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="03b86-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="03b86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03b86-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b86-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="03b86-105">DESCRIPTION</span></span>
<span data-ttu-id="03b86-106">A **Get-AzExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="03b86-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="03b86-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="03b86-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="03b86-108">Példák</span><span class="sxs-lookup"><span data-stu-id="03b86-108">EXAMPLES</span></span>

### <span data-ttu-id="03b86-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="03b86-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="03b86-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03b86-110">PARAMETERS</span></span>

### <span data-ttu-id="03b86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b86-111">-DefaultProfile</span></span>
<span data-ttu-id="03b86-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03b86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03b86-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b86-113">CommonParameters</span></span>
<span data-ttu-id="03b86-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03b86-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b86-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="03b86-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b86-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03b86-116">INPUTS</span></span>

### <span data-ttu-id="03b86-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="03b86-117">None</span></span>

## <span data-ttu-id="03b86-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03b86-118">OUTPUTS</span></span>

### <span data-ttu-id="03b86-119">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="03b86-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="03b86-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03b86-120">NOTES</span></span>

## <span data-ttu-id="03b86-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03b86-121">RELATED LINKS</span></span>

[<span data-ttu-id="03b86-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="03b86-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="03b86-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="03b86-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="03b86-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="03b86-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="03b86-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="03b86-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
