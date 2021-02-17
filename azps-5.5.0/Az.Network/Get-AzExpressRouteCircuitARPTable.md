---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147122"
---
# <span data-ttu-id="cde3a-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cde3a-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="cde3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde3a-102">SYNOPSIS</span></span>
<span data-ttu-id="cde3a-103">Az ARP-táblát egy ExpressRoute-áramkörből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cde3a-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="cde3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cde3a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cde3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cde3a-105">DESCRIPTION</span></span>
<span data-ttu-id="cde3a-106">A **Get-AzExpressRouteCircuitARPTable** parancsmag beolvassa az ARP-táblázatot egy ExpressRoute-áramkör mindkét felületéről.</span><span class="sxs-lookup"><span data-stu-id="cde3a-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="cde3a-107">Az ARP tábla az IPv4-cím MAC-címre való megfeleltetését biztosítja egy adott társviszonyhoz.</span><span class="sxs-lookup"><span data-stu-id="cde3a-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="cde3a-108">Az ARP táblázattal ellenőrizheti a 2. réteg konfigurációját és csatlakozását.</span><span class="sxs-lookup"><span data-stu-id="cde3a-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="cde3a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cde3a-109">EXAMPLES</span></span>

### <span data-ttu-id="cde3a-110">1. példa: ExpressRoute-társ ARP táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="cde3a-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="cde3a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde3a-111">PARAMETERS</span></span>

### <span data-ttu-id="cde3a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde3a-112">-DefaultProfile</span></span>
<span data-ttu-id="cde3a-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cde3a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde3a-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="cde3a-114">-DevicePath</span></span>
<span data-ttu-id="cde3a-115">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="cde3a-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="cde3a-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="cde3a-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="cde3a-117">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="cde3a-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="cde3a-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="cde3a-118">-PeeringType</span></span>
<span data-ttu-id="cde3a-119">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="cde3a-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="cde3a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde3a-120">-ResourceGroupName</span></span>
<span data-ttu-id="cde3a-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cde3a-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="cde3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde3a-122">CommonParameters</span></span>
<span data-ttu-id="cde3a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde3a-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cde3a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde3a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cde3a-125">INPUTS</span></span>

### <span data-ttu-id="cde3a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cde3a-126">System.String</span></span>

## <span data-ttu-id="cde3a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cde3a-127">OUTPUTS</span></span>

### <span data-ttu-id="cde3a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="cde3a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="cde3a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cde3a-129">NOTES</span></span>

## <span data-ttu-id="cde3a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cde3a-130">RELATED LINKS</span></span>

[<span data-ttu-id="cde3a-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cde3a-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="cde3a-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cde3a-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="cde3a-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="cde3a-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
