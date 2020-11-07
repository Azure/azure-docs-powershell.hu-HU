---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 463c1bf9e97d3e438b89cee1e87279ad4bf06ad9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670590"
---
# <span data-ttu-id="d4ce3-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d4ce3-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="d4ce3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ce3-103">Egy ExpressRoute-áramkör használati statisztikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d4ce3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4ce3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4ce3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ce3-106">A **Get-AzExpressRouteCircuitStat** parancsmag ExpressRoute-áramkör forgalmi statisztikáit keresi meg.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="d4ce3-107">A statisztika tartalmazza az elsődleges és a másodlagos útvonalon keresztül küldött és fogadott bájtok számát.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="d4ce3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d4ce3-108">EXAMPLES</span></span>

### <span data-ttu-id="d4ce3-109">Példa 1: ExpressRoute-os adatforgalmi statisztika megjelenítése</span><span class="sxs-lookup"><span data-stu-id="d4ce3-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="d4ce3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4ce3-110">PARAMETERS</span></span>

### <span data-ttu-id="d4ce3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ce3-111">-DefaultProfile</span></span>
<span data-ttu-id="d4ce3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ce3-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d4ce3-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d4ce3-114">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d4ce3-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d4ce3-115">-PeeringType</span></span>
<span data-ttu-id="d4ce3-116">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d4ce3-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d4ce3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ce3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4ce3-118">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d4ce3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ce3-119">CommonParameters</span></span>
<span data-ttu-id="d4ce3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4ce3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ce3-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4ce3-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ce3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ce3-122">INPUTS</span></span>

### <span data-ttu-id="d4ce3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ce3-123">System.String</span></span>

## <span data-ttu-id="d4ce3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ce3-124">OUTPUTS</span></span>

### <span data-ttu-id="d4ce3-125">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="d4ce3-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="d4ce3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4ce3-126">NOTES</span></span>

## <span data-ttu-id="d4ce3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4ce3-127">RELATED LINKS</span></span>

[<span data-ttu-id="d4ce3-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d4ce3-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d4ce3-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4ce3-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="d4ce3-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4ce3-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
