---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849614"
---
# <span data-ttu-id="24a74-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="24a74-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="24a74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a74-102">SYNOPSIS</span></span>
<span data-ttu-id="24a74-103">Egy ExpressRoute-áramkörből kapja meg az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="24a74-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a74-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24a74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a74-105">DESCRIPTION</span></span>
<span data-ttu-id="24a74-106">A **Get-AzureRmExpressRouteCircuitRouteTable** parancsmag egy ExpressRoute-áramkör részletes útválasztási táblázatát kéri le.</span><span class="sxs-lookup"><span data-stu-id="24a74-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="24a74-107">Az útvonaltervezés minden útvonalat megjelenít, vagy szűréssel megjelenítheti egy adott társközi típus útvonalait.</span><span class="sxs-lookup"><span data-stu-id="24a74-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="24a74-108">Az útvonaltervezés segítségével ellenőrizheti a társközi konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="24a74-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="24a74-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24a74-109">EXAMPLES</span></span>

### <span data-ttu-id="24a74-110">1. példa: az útválasztási táblázat megjelenítése az elsődleges elérési útra</span><span class="sxs-lookup"><span data-stu-id="24a74-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="24a74-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a74-111">PARAMETERS</span></span>

### <span data-ttu-id="24a74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a74-112">-DefaultProfile</span></span>
<span data-ttu-id="24a74-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a74-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a74-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="24a74-114">-DevicePath</span></span>
<span data-ttu-id="24a74-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="24a74-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a74-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="24a74-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="24a74-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="24a74-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a74-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="24a74-118">-PeeringType</span></span>
<span data-ttu-id="24a74-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="24a74-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a74-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a74-120">-ResourceGroupName</span></span>
<span data-ttu-id="24a74-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24a74-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a74-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a74-122">CommonParameters</span></span>
<span data-ttu-id="24a74-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a74-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a74-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a74-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a74-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a74-125">INPUTS</span></span>

## <span data-ttu-id="24a74-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a74-126">OUTPUTS</span></span>

### <span data-ttu-id="24a74-127">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="24a74-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="24a74-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a74-128">NOTES</span></span>

## <span data-ttu-id="24a74-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a74-129">RELATED LINKS</span></span>

[<span data-ttu-id="24a74-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="24a74-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="24a74-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="24a74-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="24a74-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="24a74-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
