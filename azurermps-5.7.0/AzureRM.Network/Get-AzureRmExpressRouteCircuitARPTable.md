---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e007f220b827db144a4c10b1adb5732e110ddf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497568"
---
# <span data-ttu-id="5f75b-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5f75b-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="5f75b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f75b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f75b-103">Az ARP-táblázatot egy ExpressRoute-áramkörről kapja.</span><span class="sxs-lookup"><span data-stu-id="5f75b-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f75b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f75b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f75b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f75b-105">DESCRIPTION</span></span>
<span data-ttu-id="5f75b-106">A **Get-AzureRmExpressRouteCircuitARPTable** PARANCSMAG az ARP-táblázatot az ExpressRoute-áramkör mindkét felületéről lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="5f75b-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="5f75b-107">Az ARP-táblázat az IPv4-cím megfeleltetését adja meg a MAC-címnek egy adott társközi számára.</span><span class="sxs-lookup"><span data-stu-id="5f75b-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="5f75b-108">Az ARP-táblázat segítségével ellenőrizheti a Layer 2 konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="5f75b-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="5f75b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5f75b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f75b-110">Példa 1: az ExpressRoute társközi ARP-táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5f75b-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="5f75b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f75b-111">PARAMETERS</span></span>

### <span data-ttu-id="5f75b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f75b-112">-DefaultProfile</span></span>
<span data-ttu-id="5f75b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f75b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f75b-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="5f75b-114">-DevicePath</span></span>
<span data-ttu-id="5f75b-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="5f75b-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="5f75b-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="5f75b-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5f75b-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="5f75b-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5f75b-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5f75b-118">-PeeringType</span></span>
<span data-ttu-id="5f75b-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5f75b-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5f75b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f75b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f75b-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5f75b-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5f75b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f75b-122">CommonParameters</span></span>
<span data-ttu-id="5f75b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f75b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f75b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f75b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f75b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f75b-125">INPUTS</span></span>

### <span data-ttu-id="5f75b-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="5f75b-126">None</span></span>
<span data-ttu-id="5f75b-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5f75b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f75b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f75b-128">OUTPUTS</span></span>

### <span data-ttu-id="5f75b-129">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="5f75b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="5f75b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f75b-130">NOTES</span></span>

## <span data-ttu-id="5f75b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f75b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f75b-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5f75b-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="5f75b-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5f75b-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5f75b-134">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5f75b-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
