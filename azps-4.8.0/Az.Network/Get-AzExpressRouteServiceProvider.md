---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184150"
---
# <span data-ttu-id="30f0a-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="30f0a-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="30f0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="30f0a-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="30f0a-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="30f0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30f0a-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30f0a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="30f0a-106">A **Get-AzExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="30f0a-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="30f0a-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="30f0a-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="30f0a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="30f0a-108">EXAMPLES</span></span>

### <span data-ttu-id="30f0a-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="30f0a-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="30f0a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30f0a-110">PARAMETERS</span></span>

### <span data-ttu-id="30f0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f0a-111">-DefaultProfile</span></span>
<span data-ttu-id="30f0a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30f0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30f0a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f0a-113">CommonParameters</span></span>
<span data-ttu-id="30f0a-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30f0a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f0a-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="30f0a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f0a-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30f0a-116">INPUTS</span></span>

### <span data-ttu-id="30f0a-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="30f0a-117">None</span></span>

## <span data-ttu-id="30f0a-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30f0a-118">OUTPUTS</span></span>

### <span data-ttu-id="30f0a-119">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="30f0a-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="30f0a-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30f0a-120">NOTES</span></span>

## <span data-ttu-id="30f0a-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30f0a-121">RELATED LINKS</span></span>

[<span data-ttu-id="30f0a-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="30f0a-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="30f0a-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="30f0a-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="30f0a-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="30f0a-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="30f0a-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="30f0a-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
