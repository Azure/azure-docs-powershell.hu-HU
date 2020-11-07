---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 590f4021fc935966e636ce92359449ea8632349a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680341"
---
# <span data-ttu-id="a8c60-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8c60-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="a8c60-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8c60-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c60-103">Egy ExpressRoute-áramkörből kapja meg az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a8c60-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c60-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8c60-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8c60-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8c60-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c60-106">A **Get-AzureRmExpressRouteCircuitRouteTable** parancsmag egy ExpressRoute-áramkör részletes útválasztási táblázatát kéri le.</span><span class="sxs-lookup"><span data-stu-id="a8c60-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="a8c60-107">Az útvonaltervezés minden útvonalat megjelenít, vagy szűréssel megjelenítheti egy adott társközi típus útvonalait.</span><span class="sxs-lookup"><span data-stu-id="a8c60-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="a8c60-108">Az útvonaltervezés segítségével ellenőrizheti a társközi konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="a8c60-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="a8c60-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a8c60-109">EXAMPLES</span></span>

### <span data-ttu-id="a8c60-110">1. példa: az útválasztási táblázat megjelenítése az elsődleges elérési útra</span><span class="sxs-lookup"><span data-stu-id="a8c60-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a8c60-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8c60-111">PARAMETERS</span></span>

### <span data-ttu-id="a8c60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c60-112">-DefaultProfile</span></span>
<span data-ttu-id="a8c60-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8c60-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c60-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a8c60-114">-DevicePath</span></span>
<span data-ttu-id="a8c60-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a8c60-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a8c60-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a8c60-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a8c60-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="a8c60-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a8c60-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a8c60-118">-PeeringType</span></span>
<span data-ttu-id="a8c60-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a8c60-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a8c60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c60-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8c60-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a8c60-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a8c60-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c60-122">CommonParameters</span></span>
<span data-ttu-id="a8c60-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8c60-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c60-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c60-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c60-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c60-125">INPUTS</span></span>

### <span data-ttu-id="a8c60-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a8c60-126">System.String</span></span>

## <span data-ttu-id="a8c60-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c60-127">OUTPUTS</span></span>

### <span data-ttu-id="a8c60-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="a8c60-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="a8c60-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8c60-129">NOTES</span></span>

## <span data-ttu-id="a8c60-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8c60-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8c60-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a8c60-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a8c60-132">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a8c60-132">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="a8c60-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="a8c60-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
