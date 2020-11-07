---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: bb6ffb1537a5beb6a845bbad742b864360da55d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670597"
---
# <span data-ttu-id="876de-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="876de-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="876de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="876de-102">SYNOPSIS</span></span>
<span data-ttu-id="876de-103">Egy ExpressRoute-áramkörből kapja meg az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="876de-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="876de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="876de-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="876de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="876de-105">DESCRIPTION</span></span>
<span data-ttu-id="876de-106">A **Get-AzExpressRouteCircuitRouteTable** parancsmag egy ExpressRoute-áramkör részletes útválasztási táblázatát kéri le.</span><span class="sxs-lookup"><span data-stu-id="876de-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="876de-107">Az útvonaltervezés minden útvonalat megjelenít, vagy szűréssel megjelenítheti egy adott társközi típus útvonalait.</span><span class="sxs-lookup"><span data-stu-id="876de-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="876de-108">Az útvonaltervezés segítségével ellenőrizheti a társközi konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="876de-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="876de-109">Példák</span><span class="sxs-lookup"><span data-stu-id="876de-109">EXAMPLES</span></span>

### <span data-ttu-id="876de-110">1. példa: az útválasztási táblázat megjelenítése az elsődleges elérési útra</span><span class="sxs-lookup"><span data-stu-id="876de-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="876de-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="876de-111">PARAMETERS</span></span>

### <span data-ttu-id="876de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876de-112">-DefaultProfile</span></span>
<span data-ttu-id="876de-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="876de-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876de-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="876de-114">-DevicePath</span></span>
<span data-ttu-id="876de-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="876de-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="876de-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="876de-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="876de-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="876de-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="876de-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="876de-118">-PeeringType</span></span>
<span data-ttu-id="876de-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="876de-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="876de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876de-120">-ResourceGroupName</span></span>
<span data-ttu-id="876de-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="876de-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="876de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876de-122">CommonParameters</span></span>
<span data-ttu-id="876de-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="876de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876de-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="876de-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876de-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="876de-125">INPUTS</span></span>

### <span data-ttu-id="876de-126">System. String</span><span class="sxs-lookup"><span data-stu-id="876de-126">System.String</span></span>

## <span data-ttu-id="876de-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="876de-127">OUTPUTS</span></span>

### <span data-ttu-id="876de-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="876de-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="876de-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="876de-129">NOTES</span></span>

## <span data-ttu-id="876de-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="876de-130">RELATED LINKS</span></span>

[<span data-ttu-id="876de-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="876de-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="876de-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="876de-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="876de-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="876de-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
