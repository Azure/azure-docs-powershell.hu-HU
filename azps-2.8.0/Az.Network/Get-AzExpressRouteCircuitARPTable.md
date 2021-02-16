---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 04c4355caaa76776a96e2619a0080b9c32d8e98a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412214"
---
# <span data-ttu-id="8bcbe-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8bcbe-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="8bcbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcbe-103">Az ARP táblázatot egy ExpressRoute-áramkörből kapja.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8bcbe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bcbe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcbe-106">A **Get-AzExpressRouteCircuitARPTable** parancsmag beolvassa az ARP táblázatot egy ExpressRoute-áramkör mindkét felületéről.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="8bcbe-107">Az ARP tábla az IPv4-cím MAC-címre való megfeleltetését biztosítja egy adott társviszonyhoz.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="8bcbe-108">Az ARP táblázattal ellenőrizheti a 2. réteg konfigurációját és csatlakozását.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="8bcbe-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8bcbe-109">EXAMPLES</span></span>

### <span data-ttu-id="8bcbe-110">1. példa: ExpressRoute-társ ARP táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="8bcbe-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="8bcbe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-111">PARAMETERS</span></span>

### <span data-ttu-id="8bcbe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcbe-112">-DefaultProfile</span></span>
<span data-ttu-id="8bcbe-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bcbe-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8bcbe-114">-DevicePath</span></span>
<span data-ttu-id="8bcbe-115">A paraméter elfogadható értékei a következőek: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8bcbe-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8bcbe-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="8bcbe-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="8bcbe-117">Az ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="8bcbe-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8bcbe-118">-PeeringType</span></span>
<span data-ttu-id="8bcbe-119">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8bcbe-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8bcbe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bcbe-120">-ResourceGroupName</span></span>
<span data-ttu-id="8bcbe-121">Az ExpressRoute-áramkört tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="8bcbe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcbe-122">CommonParameters</span></span>
<span data-ttu-id="8bcbe-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcbe-124">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bcbe-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcbe-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-125">INPUTS</span></span>

### <span data-ttu-id="8bcbe-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8bcbe-126">System.String</span></span>

## <span data-ttu-id="8bcbe-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bcbe-127">OUTPUTS</span></span>

### <span data-ttu-id="8bcbe-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="8bcbe-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="8bcbe-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8bcbe-129">NOTES</span></span>

## <span data-ttu-id="8bcbe-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bcbe-130">RELATED LINKS</span></span>

[<span data-ttu-id="8bcbe-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8bcbe-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="8bcbe-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8bcbe-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="8bcbe-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="8bcbe-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
