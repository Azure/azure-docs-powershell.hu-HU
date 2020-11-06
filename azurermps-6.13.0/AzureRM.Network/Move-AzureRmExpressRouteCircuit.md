---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: f565adcf308e9615374753a28992f572feda61ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495052"
---
# <span data-ttu-id="e5a6f-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e5a6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a6f-103">Áthelyezi a ExpressRoute-áramkört a klasszikus telepítő modellből az erőforrás-kezelő telepítő modelljébe.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5a6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5a6f-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a6f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a6f-106">Az **Áthelyezés – AzureRmExpressRouteCircuit** parancsmag áthelyezi az ExpressRoute-áramkört a klasszikus központi telepítő modellből az erőforrás-kezelő központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="e5a6f-107">Az áthelyezést követően a ExpressRoute áramköre az erőforrás-kezelő központi verziójában létrehozott bármely más ExpressRoute-áramkört elvégez és végez.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="e5a6f-108">Az áramköri hivatkozásokat, a virtuális hálózatokat és a VPN-átjárókat a művelet nem helyezi át.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="e5a6f-109">Ezeket az erőforrásokat át kell állítani az áthelyezés után.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="e5a6f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e5a6f-110">EXAMPLES</span></span>

### <span data-ttu-id="e5a6f-111">1. példa: ExpressRoute-áramkör áthelyezése az erőforrás-kezelő központi telepítő modelljébe</span><span class="sxs-lookup"><span data-stu-id="e5a6f-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="e5a6f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5a6f-112">PARAMETERS</span></span>

### <span data-ttu-id="e5a6f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5a6f-113">-AsJob</span></span>
<span data-ttu-id="e5a6f-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e5a6f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5a6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a6f-115">-DefaultProfile</span></span>
<span data-ttu-id="e5a6f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a6f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e5a6f-117">-Force</span></span>
<span data-ttu-id="e5a6f-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5a6f-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="e5a6f-119">-Location</span></span>
<span data-ttu-id="e5a6f-120">Annak az Azure-helynek a neve, ahol a ExpressRoute-áramkör lakik.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="e5a6f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5a6f-121">-Name</span></span>
<span data-ttu-id="e5a6f-122">Az áthelyezni kívánt ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="e5a6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5a6f-124">Annak az erőforráscsoportnek a neve, amely a ExpressRoute-áramkör áthelyezését fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="e5a6f-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="e5a6f-125">-ServiceKey</span></span>
<span data-ttu-id="e5a6f-126">A klasszikus telepítő modell ExpressRoute áramköre által használt szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="e5a6f-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="e5a6f-127">-Tag</span></span>
<span data-ttu-id="e5a6f-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5a6f-129">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e5a6f-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e5a6f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5a6f-130">-Confirm</span></span>
<span data-ttu-id="e5a6f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a6f-132">-WhatIf</span></span>
<span data-ttu-id="e5a6f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a6f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5a6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a6f-135">CommonParameters</span></span>
<span data-ttu-id="e5a6f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5a6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a6f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a6f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a6f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5a6f-138">INPUTS</span></span>

### <span data-ttu-id="e5a6f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a6f-139">System.String</span></span>

### <span data-ttu-id="e5a6f-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5a6f-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5a6f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5a6f-141">OUTPUTS</span></span>

### <span data-ttu-id="e5a6f-142">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e5a6f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5a6f-143">NOTES</span></span>

## <span data-ttu-id="e5a6f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5a6f-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5a6f-145">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-145">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5a6f-146">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-146">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5a6f-147">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-147">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e5a6f-148">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5a6f-148">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
