---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: ce1e05106350adda37ffa5877585ff37337dad87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670603"
---
# <span data-ttu-id="e3f8a-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e3f8a-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="e3f8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f8a-103">Az ARP-táblázatot egy ExpressRoute-áramkörről kapja.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e3f8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3f8a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f8a-106">A **Get-AzExpressRouteCircuitARPTable** PARANCSMAG az ARP-táblázatot az ExpressRoute-áramkör mindkét felületéről lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="e3f8a-107">Az ARP-táblázat az IPv4-cím megfeleltetését adja meg a MAC-címnek egy adott társközi számára.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="e3f8a-108">Az ARP-táblázat segítségével ellenőrizheti a Layer 2 konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="e3f8a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e3f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="e3f8a-110">Példa 1: az ExpressRoute társközi ARP-táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e3f8a-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="e3f8a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3f8a-111">PARAMETERS</span></span>

### <span data-ttu-id="e3f8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f8a-112">-DefaultProfile</span></span>
<span data-ttu-id="e3f8a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f8a-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="e3f8a-114">-DevicePath</span></span>
<span data-ttu-id="e3f8a-115">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="e3f8a-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="e3f8a-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="e3f8a-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="e3f8a-117">A vizsgált ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="e3f8a-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e3f8a-118">-PeeringType</span></span>
<span data-ttu-id="e3f8a-119">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e3f8a-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e3f8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3f8a-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e3f8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f8a-122">CommonParameters</span></span>
<span data-ttu-id="e3f8a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3f8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f8a-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3f8a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f8a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3f8a-125">INPUTS</span></span>

### <span data-ttu-id="e3f8a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f8a-126">System.String</span></span>

## <span data-ttu-id="e3f8a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3f8a-127">OUTPUTS</span></span>

### <span data-ttu-id="e3f8a-128">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="e3f8a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="e3f8a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3f8a-129">NOTES</span></span>

## <span data-ttu-id="e3f8a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3f8a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3f8a-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3f8a-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e3f8a-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e3f8a-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="e3f8a-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="e3f8a-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
