---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186230"
---
# <span data-ttu-id="1f291-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1f291-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="1f291-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f291-102">SYNOPSIS</span></span>
<span data-ttu-id="1f291-103">Egy ExpressRoute-áramkört tartalmazó útválasztási táblázat összefoglalását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1f291-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1f291-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f291-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f291-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f291-105">DESCRIPTION</span></span>
<span data-ttu-id="1f291-106">A **Get-AzExpressRouteCircuitRouteTableSummary** parancsmag kikeresi a BGP-szomszédok adatait egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="1f291-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="1f291-107">Ezek az információk hasznosak lehetnek annak meghatározásához, hogy mennyi időbe telik az útválasztási környezet, és hogy hány útvonal-előtagokat hirdetett meg a társ-útválasztó.</span><span class="sxs-lookup"><span data-stu-id="1f291-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="1f291-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1f291-108">EXAMPLES</span></span>

### <span data-ttu-id="1f291-109">Példa 1: az elsődleges elérési út útválasztási összegzésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="1f291-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="1f291-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f291-110">PARAMETERS</span></span>

### <span data-ttu-id="1f291-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f291-111">-DefaultProfile</span></span>
<span data-ttu-id="1f291-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f291-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f291-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1f291-113">-DevicePath</span></span>
<span data-ttu-id="1f291-114">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1f291-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1f291-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="1f291-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="1f291-116">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="1f291-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="1f291-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1f291-117">-PeeringType</span></span>
<span data-ttu-id="1f291-118">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1f291-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f291-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f291-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f291-120">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f291-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="1f291-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f291-121">CommonParameters</span></span>
<span data-ttu-id="1f291-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f291-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f291-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f291-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f291-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f291-124">INPUTS</span></span>

### <span data-ttu-id="1f291-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1f291-125">System.String</span></span>

## <span data-ttu-id="1f291-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f291-126">OUTPUTS</span></span>

### <span data-ttu-id="1f291-127">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="1f291-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="1f291-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f291-128">NOTES</span></span>

## <span data-ttu-id="1f291-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f291-129">RELATED LINKS</span></span>

[<span data-ttu-id="1f291-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1f291-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1f291-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f291-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1f291-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="1f291-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)