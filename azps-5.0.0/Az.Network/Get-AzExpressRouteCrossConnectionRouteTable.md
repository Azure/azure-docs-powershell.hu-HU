---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195673"
---
# <span data-ttu-id="7b219-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7b219-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="7b219-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b219-102">SYNOPSIS</span></span>
<span data-ttu-id="7b219-103">Útválasztási táblázatot kap egy ExpressRoute-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="7b219-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7b219-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b219-104">SYNTAX</span></span>

### <span data-ttu-id="7b219-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="7b219-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b219-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="7b219-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b219-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b219-107">DESCRIPTION</span></span>
<span data-ttu-id="7b219-108">A **Get-AzExpressRouteCrossConnectionRouteTable** parancsmag egy ExpressRoute-áramkör részletes útválasztási táblázatát kéri le.</span><span class="sxs-lookup"><span data-stu-id="7b219-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="7b219-109">Az útvonaltervezés minden útvonalat megjelenít, vagy szűréssel megjelenítheti egy adott társközi típus útvonalait.</span><span class="sxs-lookup"><span data-stu-id="7b219-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="7b219-110">Az útvonaltervezés segítségével ellenőrizheti a társközi konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="7b219-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="7b219-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7b219-111">EXAMPLES</span></span>

### <span data-ttu-id="7b219-112">1. példa: az útválasztási táblázat megjelenítése az elsődleges elérési útra</span><span class="sxs-lookup"><span data-stu-id="7b219-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="7b219-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b219-113">PARAMETERS</span></span>

### <span data-ttu-id="7b219-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="7b219-114">-CrossConnectionName</span></span>
<span data-ttu-id="7b219-115">Az Express Route Cross Connection kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="7b219-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b219-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b219-116">-DefaultProfile</span></span>
<span data-ttu-id="7b219-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b219-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b219-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7b219-118">-DevicePath</span></span>
<span data-ttu-id="7b219-119">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7b219-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7b219-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b219-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7b219-121">Az Express Route Cross kapcsolat</span><span class="sxs-lookup"><span data-stu-id="7b219-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b219-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7b219-122">-PeeringType</span></span>
<span data-ttu-id="7b219-123">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7b219-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7b219-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b219-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b219-125">Az ExpressRoute-kapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7b219-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b219-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b219-126">CommonParameters</span></span>
<span data-ttu-id="7b219-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b219-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b219-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7b219-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b219-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b219-129">INPUTS</span></span>

### <span data-ttu-id="7b219-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="7b219-130">None</span></span>
<span data-ttu-id="7b219-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7b219-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b219-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b219-132">OUTPUTS</span></span>

### <span data-ttu-id="7b219-133">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="7b219-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="7b219-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b219-134">NOTES</span></span>

## <span data-ttu-id="7b219-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b219-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b219-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="7b219-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="7b219-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7b219-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)