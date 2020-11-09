---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302048"
---
# <span data-ttu-id="1e080-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e080-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="1e080-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e080-102">SYNOPSIS</span></span>
<span data-ttu-id="1e080-103">Beolvassa a ExpressRoute-kapcsolat útválasztási táblázatát.</span><span class="sxs-lookup"><span data-stu-id="1e080-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1e080-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e080-104">SYNTAX</span></span>

### <span data-ttu-id="1e080-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1e080-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e080-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="1e080-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e080-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e080-107">DESCRIPTION</span></span>
<span data-ttu-id="1e080-108">A **Get-AzExpressRouteCrossConnectionRouteTableSummary** parancsmag kikeresi a BGP-szomszédok adatait egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="1e080-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="1e080-109">Ezek az információk hasznosak lehetnek annak meghatározásához, hogy mennyi időbe telik az útválasztási környezet, és hogy hány útvonal-előtagokat hirdetett meg a társ-útválasztó.</span><span class="sxs-lookup"><span data-stu-id="1e080-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="1e080-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e080-110">EXAMPLES</span></span>

### <span data-ttu-id="1e080-111">Példa 1: az elsődleges elérési út útválasztási összegzésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="1e080-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="1e080-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e080-112">PARAMETERS</span></span>

### <span data-ttu-id="1e080-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="1e080-113">-CrossConnectionName</span></span>
<span data-ttu-id="1e080-114">Az Express Route Cross Connection kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="1e080-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="1e080-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e080-115">-DefaultProfile</span></span>
<span data-ttu-id="1e080-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e080-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e080-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1e080-117">-DevicePath</span></span>
<span data-ttu-id="1e080-118">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1e080-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1e080-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1e080-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1e080-120">Az Express Route Cross kapcsolat</span><span class="sxs-lookup"><span data-stu-id="1e080-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="1e080-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1e080-121">-PeeringType</span></span>
<span data-ttu-id="1e080-122">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1e080-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1e080-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e080-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e080-124">Az ExpressRoute-kapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e080-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="1e080-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e080-125">CommonParameters</span></span>
<span data-ttu-id="1e080-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e080-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e080-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e080-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e080-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e080-128">INPUTS</span></span>

### <span data-ttu-id="1e080-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e080-129">None</span></span>
<span data-ttu-id="1e080-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1e080-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e080-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e080-131">OUTPUTS</span></span>

### <span data-ttu-id="1e080-132">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e080-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="1e080-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e080-133">NOTES</span></span>

## <span data-ttu-id="1e080-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e080-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e080-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="1e080-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="1e080-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e080-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
