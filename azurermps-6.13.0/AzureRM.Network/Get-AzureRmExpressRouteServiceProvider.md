---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: 0c7beb4bc53635a8bf4293abf50441b0f15b66b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680330"
---
# <span data-ttu-id="34c27-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="34c27-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="34c27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34c27-102">SYNOPSIS</span></span>
<span data-ttu-id="34c27-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="34c27-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34c27-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c27-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34c27-105">DESCRIPTION</span></span>
<span data-ttu-id="34c27-106">A **Get-AzureRmExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="34c27-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="34c27-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="34c27-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="34c27-108">Példák</span><span class="sxs-lookup"><span data-stu-id="34c27-108">EXAMPLES</span></span>

### <span data-ttu-id="34c27-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="34c27-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="34c27-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34c27-110">PARAMETERS</span></span>

### <span data-ttu-id="34c27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c27-111">-DefaultProfile</span></span>
<span data-ttu-id="34c27-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34c27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c27-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c27-113">CommonParameters</span></span>
<span data-ttu-id="34c27-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34c27-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c27-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c27-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c27-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c27-116">INPUTS</span></span>

### <span data-ttu-id="34c27-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="34c27-117">None</span></span>

## <span data-ttu-id="34c27-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c27-118">OUTPUTS</span></span>

### <span data-ttu-id="34c27-119">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="34c27-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="34c27-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34c27-120">NOTES</span></span>

## <span data-ttu-id="34c27-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c27-121">RELATED LINKS</span></span>

[<span data-ttu-id="34c27-122">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="34c27-122">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="34c27-123">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="34c27-123">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="34c27-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="34c27-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="34c27-125">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="34c27-125">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
