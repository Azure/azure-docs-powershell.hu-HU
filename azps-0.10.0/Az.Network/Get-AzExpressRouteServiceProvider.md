---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: ce3d4e42c6644cd3181ec9389a7b571c7f6ca51a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841642"
---
# <span data-ttu-id="47859-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="47859-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="47859-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47859-102">SYNOPSIS</span></span>
<span data-ttu-id="47859-103">Beolvassa a List ExpressRoute szolgáltatókat és attribútumaikat.</span><span class="sxs-lookup"><span data-stu-id="47859-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="47859-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47859-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47859-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47859-105">DESCRIPTION</span></span>
<span data-ttu-id="47859-106">A **Get-AzExpressRouteServiceProvider** parancsmag kikeresi a ExpressRoute-szolgáltatókat és a hozzájuk tartozó attribútumokat.</span><span class="sxs-lookup"><span data-stu-id="47859-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="47859-107">Az attribútum a hely és a sávszélesség beállítását is tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="47859-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="47859-108">Példák</span><span class="sxs-lookup"><span data-stu-id="47859-108">EXAMPLES</span></span>

### <span data-ttu-id="47859-109">Példa 1: szolgáltató listája a "Silicon Valley" helyekkel</span><span class="sxs-lookup"><span data-stu-id="47859-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="47859-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47859-110">PARAMETERS</span></span>

### <span data-ttu-id="47859-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47859-111">-DefaultProfile</span></span>
<span data-ttu-id="47859-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47859-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47859-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47859-113">CommonParameters</span></span>
<span data-ttu-id="47859-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47859-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47859-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47859-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47859-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47859-116">INPUTS</span></span>

## <span data-ttu-id="47859-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47859-117">OUTPUTS</span></span>

### <span data-ttu-id="47859-118">Microsoft. Azure. commands. Network. models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="47859-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="47859-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47859-119">NOTES</span></span>

## <span data-ttu-id="47859-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47859-120">RELATED LINKS</span></span>

[<span data-ttu-id="47859-121">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="47859-121">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="47859-122">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="47859-122">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="47859-123">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47859-123">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="47859-124">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="47859-124">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
