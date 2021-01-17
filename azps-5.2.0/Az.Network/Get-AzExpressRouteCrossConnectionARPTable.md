---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329766"
---
# <span data-ttu-id="37f63-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="37f63-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="37f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f63-102">SYNOPSIS</span></span>
<span data-ttu-id="37f63-103">Az ARP táblát ExpressRoute-kapcsolaton keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="37f63-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="37f63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37f63-104">SYNTAX</span></span>

### <span data-ttu-id="37f63-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="37f63-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37f63-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="37f63-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37f63-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37f63-107">DESCRIPTION</span></span>
<span data-ttu-id="37f63-108">A **Get-AzExpressRouteCrossConnectionARPTable** parancsmag beolvassa az ARP táblázatot egy ExpressRoute-keresztkapcsolat mindkét felületéről.</span><span class="sxs-lookup"><span data-stu-id="37f63-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="37f63-109">Az ARP táblázat az IPv4-cím MAC-címre való megfeleltetését biztosítja egy adott társviszonyhoz.</span><span class="sxs-lookup"><span data-stu-id="37f63-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="37f63-110">Az ARP táblázattal ellenőrizheti a 2. réteg konfigurációját és csatlakozását.</span><span class="sxs-lookup"><span data-stu-id="37f63-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="37f63-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37f63-111">EXAMPLES</span></span>

### <span data-ttu-id="37f63-112">1. példa: ExpressRoute-társ ARP táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="37f63-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="37f63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37f63-113">PARAMETERS</span></span>

### <span data-ttu-id="37f63-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="37f63-114">-CrossConnectionName</span></span>
<span data-ttu-id="37f63-115">Az Express Route Cross Connection neve</span><span class="sxs-lookup"><span data-stu-id="37f63-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="37f63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f63-116">-DefaultProfile</span></span>
<span data-ttu-id="37f63-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37f63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f63-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="37f63-118">-DevicePath</span></span>
<span data-ttu-id="37f63-119">A paraméter elfogadható értékei: `Primary` vagy `Secondary`</span><span class="sxs-lookup"><span data-stu-id="37f63-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="37f63-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="37f63-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="37f63-121">The Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="37f63-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="37f63-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="37f63-122">-PeeringType</span></span>
<span data-ttu-id="37f63-123">A paraméter elfogadható értékei a következőek: `AzurePrivatePeering` `AzurePublicPeering` , és `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="37f63-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="37f63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f63-124">-ResourceGroupName</span></span>
<span data-ttu-id="37f63-125">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37f63-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="37f63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f63-126">CommonParameters</span></span>
<span data-ttu-id="37f63-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f63-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37f63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f63-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37f63-129">INPUTS</span></span>

### <span data-ttu-id="37f63-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="37f63-130">None</span></span>
<span data-ttu-id="37f63-131">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="37f63-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37f63-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37f63-132">OUTPUTS</span></span>

### <span data-ttu-id="37f63-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="37f63-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="37f63-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37f63-134">NOTES</span></span>

## <span data-ttu-id="37f63-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37f63-135">RELATED LINKS</span></span>

[<span data-ttu-id="37f63-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="37f63-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="37f63-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="37f63-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
