---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 43bf5a0a551840d03ac19e9ea78b26135dde5493
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841674"
---
# <span data-ttu-id="b04ea-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b04ea-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="b04ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b04ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b04ea-103">Az ARP-táblázatot egy ExpressRoute-áramkörről kapja.</span><span class="sxs-lookup"><span data-stu-id="b04ea-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b04ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b04ea-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b04ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b04ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b04ea-106">A **Get-AzExpressRouteCircuitARPTable** PARANCSMAG az ARP-táblázatot az ExpressRoute-áramkör mindkét felületéről lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="b04ea-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="b04ea-107">Az ARP-táblázat az IPv4-cím megfeleltetését adja meg a MAC-címnek egy adott társközi számára.</span><span class="sxs-lookup"><span data-stu-id="b04ea-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="b04ea-108">Az ARP-táblázat segítségével ellenőrizheti a Layer 2 konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="b04ea-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="b04ea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b04ea-109">EXAMPLES</span></span>

### <span data-ttu-id="b04ea-110">Példa 1: az ExpressRoute társközi ARP-táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="b04ea-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="b04ea-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b04ea-111">PARAMETERS</span></span>

### <span data-ttu-id="b04ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04ea-112">-DefaultProfile</span></span>
<span data-ttu-id="b04ea-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b04ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04ea-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b04ea-114">-DevicePath</span></span>
<span data-ttu-id="b04ea-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b04ea-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="b04ea-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="b04ea-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b04ea-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="b04ea-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="b04ea-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b04ea-118">-PeeringType</span></span>
<span data-ttu-id="b04ea-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b04ea-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b04ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="b04ea-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b04ea-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b04ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04ea-122">CommonParameters</span></span>
<span data-ttu-id="b04ea-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b04ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04ea-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04ea-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04ea-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b04ea-125">INPUTS</span></span>

## <span data-ttu-id="b04ea-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b04ea-126">OUTPUTS</span></span>

### <span data-ttu-id="b04ea-127">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="b04ea-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="b04ea-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b04ea-128">NOTES</span></span>

## <span data-ttu-id="b04ea-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b04ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="b04ea-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b04ea-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b04ea-131">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b04ea-131">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b04ea-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="b04ea-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
