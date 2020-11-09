---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300641"
---
# <span data-ttu-id="0f314-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="0f314-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f314-102">SYNOPSIS</span></span>
<span data-ttu-id="0f314-103">Áthelyezi a ExpressRoute-áramkört a klasszikus telepítő modellből az erőforrás-kezelő telepítő modelljébe.</span><span class="sxs-lookup"><span data-stu-id="0f314-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="0f314-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f314-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f314-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f314-105">DESCRIPTION</span></span>
<span data-ttu-id="0f314-106">Az **Áthelyezés – AzExpressRouteCircuit** parancsmag áthelyezi az ExpressRoute-áramkört a klasszikus központi telepítő modellből az erőforrás-kezelő központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="0f314-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="0f314-107">Az áthelyezést követően a ExpressRoute áramköre az erőforrás-kezelő központi verziójában létrehozott bármely más ExpressRoute-áramkört elvégez és végez.</span><span class="sxs-lookup"><span data-stu-id="0f314-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="0f314-108">Az áramköri hivatkozásokat, a virtuális hálózatokat és a VPN-átjárókat a művelet nem helyezi át.</span><span class="sxs-lookup"><span data-stu-id="0f314-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="0f314-109">Ezeket az erőforrásokat át kell állítani az áthelyezés után.</span><span class="sxs-lookup"><span data-stu-id="0f314-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="0f314-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f314-110">EXAMPLES</span></span>

### <span data-ttu-id="0f314-111">1. példa: ExpressRoute-áramkör áthelyezése az erőforrás-kezelő központi telepítő modelljébe</span><span class="sxs-lookup"><span data-stu-id="0f314-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="0f314-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f314-112">PARAMETERS</span></span>

### <span data-ttu-id="0f314-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f314-113">-AsJob</span></span>
<span data-ttu-id="0f314-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f314-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f314-115">-DefaultProfile</span></span>
<span data-ttu-id="0f314-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f314-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f314-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0f314-117">-Force</span></span>
<span data-ttu-id="0f314-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0f314-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="0f314-119">-Location</span></span>
<span data-ttu-id="0f314-120">Annak az Azure-helynek a neve, ahol a ExpressRoute-áramkör lakik.</span><span class="sxs-lookup"><span data-stu-id="0f314-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="0f314-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f314-121">-Name</span></span>
<span data-ttu-id="0f314-122">Az áthelyezni kívánt ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="0f314-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f314-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f314-124">Annak az erőforráscsoportnek a neve, amely a ExpressRoute-áramkör áthelyezését fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0f314-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="0f314-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="0f314-125">-ServiceKey</span></span>
<span data-ttu-id="0f314-126">A klasszikus telepítő modell ExpressRoute áramköre által használt szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="0f314-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="0f314-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="0f314-127">-Tag</span></span>
<span data-ttu-id="0f314-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0f314-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f314-129">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0f314-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f314-130">-Confirm</span></span>
<span data-ttu-id="0f314-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f314-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f314-132">-WhatIf</span></span>
<span data-ttu-id="0f314-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f314-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f314-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f314-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f314-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f314-135">CommonParameters</span></span>
<span data-ttu-id="0f314-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f314-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f314-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f314-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f314-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f314-138">INPUTS</span></span>

### <span data-ttu-id="0f314-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0f314-139">System.String</span></span>

### <span data-ttu-id="0f314-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f314-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0f314-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f314-141">OUTPUTS</span></span>

### <span data-ttu-id="0f314-142">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0f314-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f314-143">NOTES</span></span>

## <span data-ttu-id="0f314-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f314-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f314-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f314-146">Új – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f314-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="0f314-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0f314-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
