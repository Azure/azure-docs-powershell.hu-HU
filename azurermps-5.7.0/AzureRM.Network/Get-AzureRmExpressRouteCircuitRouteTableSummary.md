---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497564"
---
# <span data-ttu-id="66bf0-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="66bf0-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="66bf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="66bf0-103">Egy ExpressRoute-áramkört tartalmazó útválasztási táblázat összefoglalását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66bf0-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66bf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66bf0-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66bf0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="66bf0-106">A **Get-AzureRmExpressRouteCircuitRouteTableSummary** parancsmag kikeresi a BGP-szomszédok adatait egy adott útválasztási környezetben.</span><span class="sxs-lookup"><span data-stu-id="66bf0-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="66bf0-107">Ezek az információk hasznosak lehetnek annak meghatározásához, hogy mennyi időbe telik az útválasztási környezet, és hogy hány útvonal-előtagokat hirdetett meg a társ-útválasztó.</span><span class="sxs-lookup"><span data-stu-id="66bf0-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="66bf0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="66bf0-108">EXAMPLES</span></span>

### <span data-ttu-id="66bf0-109">Példa 1: az elsődleges elérési út útválasztási összegzésének megjelenítése</span><span class="sxs-lookup"><span data-stu-id="66bf0-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="66bf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="66bf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bf0-111">-DefaultProfile</span></span>
<span data-ttu-id="66bf0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66bf0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66bf0-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="66bf0-113">-DevicePath</span></span>
<span data-ttu-id="66bf0-114">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="66bf0-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="66bf0-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="66bf0-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="66bf0-116">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="66bf0-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="66bf0-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="66bf0-117">-PeeringType</span></span>
<span data-ttu-id="66bf0-118">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="66bf0-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="66bf0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bf0-119">-ResourceGroupName</span></span>
<span data-ttu-id="66bf0-120">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66bf0-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="66bf0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bf0-121">CommonParameters</span></span>
<span data-ttu-id="66bf0-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66bf0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bf0-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bf0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bf0-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66bf0-124">INPUTS</span></span>

### <span data-ttu-id="66bf0-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="66bf0-125">None</span></span>
<span data-ttu-id="66bf0-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="66bf0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66bf0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66bf0-127">OUTPUTS</span></span>

### <span data-ttu-id="66bf0-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="66bf0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="66bf0-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66bf0-129">NOTES</span></span>

## <span data-ttu-id="66bf0-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66bf0-130">RELATED LINKS</span></span>

[<span data-ttu-id="66bf0-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="66bf0-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="66bf0-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="66bf0-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="66bf0-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="66bf0-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
