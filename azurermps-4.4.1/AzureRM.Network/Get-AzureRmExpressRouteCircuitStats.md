---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 3230a9e9d8bb70cc80125258cca7d2eaef973e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500807"
---
# <span data-ttu-id="55073-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="55073-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="55073-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55073-102">SYNOPSIS</span></span>
<span data-ttu-id="55073-103">Egy ExpressRoute-áramkör használati statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="55073-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55073-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55073-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55073-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55073-105">DESCRIPTION</span></span>
<span data-ttu-id="55073-106">A **Get-AzureRmExpressRouteCircuitStats** parancsmag ExpressRoute-áramkör forgalmi statisztikáit keresi meg.</span><span class="sxs-lookup"><span data-stu-id="55073-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="55073-107">A statisztika tartalmazza az elsődleges és a másodlagos útvonalon keresztül küldött és fogadott bájtok számát.</span><span class="sxs-lookup"><span data-stu-id="55073-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="55073-108">Példák</span><span class="sxs-lookup"><span data-stu-id="55073-108">EXAMPLES</span></span>

### <span data-ttu-id="55073-109">Példa 1: ExpressRoute-os adatforgalmi statisztika megjelenítése</span><span class="sxs-lookup"><span data-stu-id="55073-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="55073-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55073-110">PARAMETERS</span></span>

### <span data-ttu-id="55073-111">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="55073-111">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="55073-112">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="55073-112">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="55073-113">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="55073-113">-PeeringType</span></span>
<span data-ttu-id="55073-114">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="55073-114">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="55073-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55073-115">-ResourceGroupName</span></span>
<span data-ttu-id="55073-116">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="55073-116">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="55073-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55073-117">-DefaultProfile</span></span>
<span data-ttu-id="55073-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55073-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55073-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55073-119">CommonParameters</span></span>
<span data-ttu-id="55073-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55073-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55073-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55073-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55073-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55073-122">INPUTS</span></span>

## <span data-ttu-id="55073-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55073-123">OUTPUTS</span></span>

### <span data-ttu-id="55073-124">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="55073-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="55073-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55073-125">NOTES</span></span>

## <span data-ttu-id="55073-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55073-126">RELATED LINKS</span></span>

[<span data-ttu-id="55073-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="55073-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="55073-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="55073-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="55073-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="55073-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
