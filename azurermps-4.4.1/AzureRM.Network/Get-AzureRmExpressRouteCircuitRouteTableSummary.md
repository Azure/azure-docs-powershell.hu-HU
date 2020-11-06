---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: b4e93b89a11d4341b6a04de1b5625084e9348c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500808"
---
# <span data-ttu-id="f3e26-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f3e26-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="f3e26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3e26-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e26-103">Egy ExpressRoute-áramkört tartalmazó útválasztási táblázat összefoglalását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f3e26-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3e26-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3e26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3e26-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e26-106">A **Get-AzureRmExpressRouteCircuitRouteTableSummary** parancsmag kikeresi a BGP-szomszédok adatait egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="f3e26-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="f3e26-107">Ezek az információk hasznosak lehetnek annak meghatározásához, hogy mennyi időbe telik az útválasztási környezet, és hogy hány útvonal-előtagokat hirdetett meg a társ-útválasztó.</span><span class="sxs-lookup"><span data-stu-id="f3e26-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="f3e26-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f3e26-108">EXAMPLES</span></span>

### <span data-ttu-id="f3e26-109">Példa 1: az elsődleges elérési út útválasztási összegzésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="f3e26-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f3e26-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3e26-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e26-111">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f3e26-111">-DevicePath</span></span>
<span data-ttu-id="f3e26-112">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f3e26-112">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e26-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f3e26-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f3e26-114">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="f3e26-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f3e26-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f3e26-115">-PeeringType</span></span>
<span data-ttu-id="f3e26-116">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f3e26-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f3e26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e26-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3e26-118">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f3e26-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f3e26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e26-119">-DefaultProfile</span></span>
<span data-ttu-id="f3e26-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3e26-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e26-121">CommonParameters</span></span>
<span data-ttu-id="f3e26-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3e26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e26-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e26-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e26-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e26-124">INPUTS</span></span>

## <span data-ttu-id="f3e26-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3e26-125">OUTPUTS</span></span>

### <span data-ttu-id="f3e26-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="f3e26-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="f3e26-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3e26-127">NOTES</span></span>

## <span data-ttu-id="f3e26-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3e26-128">RELATED LINKS</span></span>

[<span data-ttu-id="f3e26-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f3e26-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f3e26-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f3e26-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f3e26-131">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f3e26-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
