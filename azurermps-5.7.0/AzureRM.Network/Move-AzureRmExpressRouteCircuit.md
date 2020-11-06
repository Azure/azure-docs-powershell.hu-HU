---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: d0fb9fb0c6fb27ff683fcbb2b3ae537d736189cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496415"
---
# <span data-ttu-id="5e2d3-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="5e2d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2d3-103">Áthelyezi a ExpressRoute-áramkört a klasszikus telepítő modellből az erőforrás-kezelő telepítő modelljébe.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e2d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e2d3-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e2d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="5e2d3-106">Az **Áthelyezés – AzureRmExpressRouteCircuit** parancsmag áthelyezi az ExpressRoute-áramkört a klasszikus központi telepítő modellből az erőforrás-kezelő központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="5e2d3-107">Az áthelyezést követően a ExpressRoute áramköre az erőforrás-kezelő központi verziójában létrehozott bármely más ExpressRoute-áramkört elvégez és végez.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="5e2d3-108">Az áramköri hivatkozásokat, a virtuális hálózatokat és a VPN-átjárókat a művelet nem helyezi át.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="5e2d3-109">Ezeket az erőforrásokat át kell állítani az áthelyezés után.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="5e2d3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5e2d3-110">EXAMPLES</span></span>

### <span data-ttu-id="5e2d3-111">1. példa: ExpressRoute-áramkör áthelyezése az erőforrás-kezelő központi telepítő modelljébe</span><span class="sxs-lookup"><span data-stu-id="5e2d3-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="5e2d3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e2d3-112">PARAMETERS</span></span>

### <span data-ttu-id="5e2d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e2d3-113">-AsJob</span></span>
<span data-ttu-id="5e2d3-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5e2d3-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2d3-115">-DefaultProfile</span></span>
<span data-ttu-id="5e2d3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e2d3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5e2d3-117">-Force</span></span>
<span data-ttu-id="5e2d3-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="5e2d3-119">-Location</span></span>
<span data-ttu-id="5e2d3-120">Annak az Azure-helynek a neve, ahol a ExpressRoute-áramkör lakik.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="5e2d3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e2d3-121">-Name</span></span>
<span data-ttu-id="5e2d3-122">Az áthelyezni kívánt ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e2d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e2d3-124">Annak az erőforráscsoportnek a neve, amely a ExpressRoute-áramkör áthelyezését fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="5e2d3-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="5e2d3-125">-ServiceKey</span></span>
<span data-ttu-id="5e2d3-126">A klasszikus telepítő modell ExpressRoute áramköre által használt szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="5e2d3-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="5e2d3-127">-Tag</span></span>
<span data-ttu-id="5e2d3-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e2d3-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="5e2d3-129">For example:</span></span>

<span data-ttu-id="5e2d3-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5e2d3-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e2d3-131">-Confirm</span></span>
<span data-ttu-id="5e2d3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e2d3-133">-WhatIf</span></span>
<span data-ttu-id="5e2d3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e2d3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2d3-136">CommonParameters</span></span>
<span data-ttu-id="5e2d3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e2d3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2d3-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2d3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2d3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e2d3-139">INPUTS</span></span>

### <span data-ttu-id="5e2d3-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e2d3-140">None</span></span>
<span data-ttu-id="5e2d3-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5e2d3-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e2d3-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e2d3-142">OUTPUTS</span></span>

### <span data-ttu-id="5e2d3-143">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5e2d3-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e2d3-144">NOTES</span></span>

## <span data-ttu-id="5e2d3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e2d3-145">RELATED LINKS</span></span>

[<span data-ttu-id="5e2d3-146">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-146">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e2d3-147">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-147">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e2d3-148">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-148">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5e2d3-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5e2d3-149">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
