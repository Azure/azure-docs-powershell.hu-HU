---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849214"
---
# <span data-ttu-id="f5a5f-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f5a5f-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f5a5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a5f-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5a5f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a5f-106">A **Get-AzureRmExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="f5a5f-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="f5a5f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f5a5f-108">EXAMPLES</span></span>

### <span data-ttu-id="f5a5f-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="f5a5f-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="f5a5f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a5f-111">-DefaultProfile</span></span>
<span data-ttu-id="f5a5f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a5f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a5f-113">CommonParameters</span></span>
<span data-ttu-id="f5a5f-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5a5f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a5f-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a5f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a5f-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5a5f-116">INPUTS</span></span>

## <span data-ttu-id="f5a5f-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5a5f-117">OUTPUTS</span></span>

### <span data-ttu-id="f5a5f-118">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f5a5f-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f5a5f-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5a5f-119">NOTES</span></span>

## <span data-ttu-id="f5a5f-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5a5f-120">RELATED LINKS</span></span>

[<span data-ttu-id="f5a5f-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f5a5f-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f5a5f-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5a5f-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f5a5f-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5a5f-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f5a5f-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f5a5f-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
