---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 3d7068eaa469779c3a7b02095f30d4ea3178dd6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670583"
---
# <span data-ttu-id="41e6a-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="41e6a-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="41e6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="41e6a-103">Az ARP-táblázatot egy ExpressRoute-kapcsolaton keresztül kapja.</span><span class="sxs-lookup"><span data-stu-id="41e6a-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="41e6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41e6a-104">SYNTAX</span></span>

### <span data-ttu-id="41e6a-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="41e6a-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41e6a-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="41e6a-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41e6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41e6a-107">DESCRIPTION</span></span>
<span data-ttu-id="41e6a-108">A **Get-AzExpressRouteCrossConnectionARPTable** PARANCSMAG az ARP-táblázatot az ExpressRoute-kapcsolat két felületéről is lekérdezi.</span><span class="sxs-lookup"><span data-stu-id="41e6a-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="41e6a-109">Az ARP-táblázat az IPv4-cím megfeleltetését adja meg a MAC-címnek egy adott társközi számára.</span><span class="sxs-lookup"><span data-stu-id="41e6a-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="41e6a-110">Az ARP-táblázat segítségével ellenőrizheti a Layer 2 konfigurációt és a kapcsolódást.</span><span class="sxs-lookup"><span data-stu-id="41e6a-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="41e6a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41e6a-111">EXAMPLES</span></span>

### <span data-ttu-id="41e6a-112">Példa 1: az ExpressRoute társközi ARP-táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="41e6a-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="41e6a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41e6a-113">PARAMETERS</span></span>

### <span data-ttu-id="41e6a-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="41e6a-114">-CrossConnectionName</span></span>
<span data-ttu-id="41e6a-115">Az Express Route Cross Connection kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="41e6a-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="41e6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e6a-116">-DefaultProfile</span></span>
<span data-ttu-id="41e6a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41e6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41e6a-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="41e6a-118">-DevicePath</span></span>
<span data-ttu-id="41e6a-119">A paraméter elfogadható értékei a következők: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="41e6a-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="41e6a-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="41e6a-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="41e6a-121">Az Express Route Cross kapcsolat</span><span class="sxs-lookup"><span data-stu-id="41e6a-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="41e6a-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="41e6a-122">-PeeringType</span></span>
<span data-ttu-id="41e6a-123">A paraméter elfogadható értékei a következők: `AzurePrivatePeering` , `AzurePublicPeering` és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="41e6a-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="41e6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="41e6a-125">Az ExpressRoute-kapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41e6a-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="41e6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e6a-126">CommonParameters</span></span>
<span data-ttu-id="41e6a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41e6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e6a-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41e6a-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e6a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41e6a-129">INPUTS</span></span>

### <span data-ttu-id="41e6a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="41e6a-130">None</span></span>
<span data-ttu-id="41e6a-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="41e6a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41e6a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41e6a-132">OUTPUTS</span></span>

### <span data-ttu-id="41e6a-133">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="41e6a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="41e6a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41e6a-134">NOTES</span></span>

## <span data-ttu-id="41e6a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41e6a-135">RELATED LINKS</span></span>

[<span data-ttu-id="41e6a-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="41e6a-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="41e6a-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="41e6a-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
