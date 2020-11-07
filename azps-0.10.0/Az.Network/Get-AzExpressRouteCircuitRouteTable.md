---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 99f73d9a24ab18c244e4122e5dca7dce0d4002d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841649"
---
# <span data-ttu-id="dd53b-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd53b-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="dd53b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dd53b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd53b-103">Egy ExpressRoute-áramkörből kapja meg az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="dd53b-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="dd53b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dd53b-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd53b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dd53b-105">DESCRIPTION</span></span>
<span data-ttu-id="dd53b-106">A **Get-AzExpressRouteCircuitRouteTable** parancsmag egy ExpressRoute-áramkör részletes útválasztási táblázatát kéri le.</span><span class="sxs-lookup"><span data-stu-id="dd53b-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="dd53b-107">Az útvonaltervezés minden útvonalat megjelenít, vagy szűréssel megjelenítheti egy adott társközi típus útvonalait.</span><span class="sxs-lookup"><span data-stu-id="dd53b-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="dd53b-108">Az útvonaltervezés segítségével ellenőrizheti a társközi konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="dd53b-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="dd53b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dd53b-109">EXAMPLES</span></span>

### <span data-ttu-id="dd53b-110">1. példa: az útválasztási táblázat megjelenítése az elsődleges elérési útra</span><span class="sxs-lookup"><span data-stu-id="dd53b-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="dd53b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dd53b-111">PARAMETERS</span></span>

### <span data-ttu-id="dd53b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd53b-112">-DefaultProfile</span></span>
<span data-ttu-id="dd53b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd53b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd53b-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="dd53b-114">-DevicePath</span></span>
<span data-ttu-id="dd53b-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="dd53b-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="dd53b-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="dd53b-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="dd53b-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="dd53b-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="dd53b-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dd53b-118">-PeeringType</span></span>
<span data-ttu-id="dd53b-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dd53b-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="dd53b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd53b-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd53b-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dd53b-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="dd53b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd53b-122">CommonParameters</span></span>
<span data-ttu-id="dd53b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dd53b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd53b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd53b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd53b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd53b-125">INPUTS</span></span>

## <span data-ttu-id="dd53b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd53b-126">OUTPUTS</span></span>

### <span data-ttu-id="dd53b-127">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="dd53b-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="dd53b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dd53b-128">NOTES</span></span>

## <span data-ttu-id="dd53b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd53b-129">RELATED LINKS</span></span>

[<span data-ttu-id="dd53b-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dd53b-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="dd53b-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd53b-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="dd53b-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="dd53b-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
