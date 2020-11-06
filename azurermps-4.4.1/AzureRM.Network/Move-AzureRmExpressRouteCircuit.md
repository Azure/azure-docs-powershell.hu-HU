---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499960"
---
# <span data-ttu-id="acaa1-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="acaa1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="acaa1-103">Áthelyezi a ExpressRoute-áramkört a klasszikus telepítő modellből az erőforrás-kezelő telepítő modelljébe.</span><span class="sxs-lookup"><span data-stu-id="acaa1-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acaa1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acaa1-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acaa1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="acaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="acaa1-106">Az **Áthelyezés – AzureRmExpressRouteCircuit** parancsmag áthelyezi az ExpressRoute-áramkört a klasszikus központi telepítő modellből az erőforrás-kezelő központi verzióba.</span><span class="sxs-lookup"><span data-stu-id="acaa1-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="acaa1-107">Az áthelyezést követően a ExpressRoute áramköre az erőforrás-kezelő központi verziójában létrehozott bármely más ExpressRoute-áramkört elvégez és végez.</span><span class="sxs-lookup"><span data-stu-id="acaa1-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="acaa1-108">Az áramköri hivatkozásokat, a virtuális hálózatokat és a VPN-átjárókat a művelet nem helyezi át.</span><span class="sxs-lookup"><span data-stu-id="acaa1-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="acaa1-109">Ezeket az erőforrásokat át kell állítani az áthelyezés után.</span><span class="sxs-lookup"><span data-stu-id="acaa1-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="acaa1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="acaa1-110">EXAMPLES</span></span>

### <span data-ttu-id="acaa1-111">1. példa: ExpressRoute-áramkör áthelyezése az erőforrás-kezelő központi telepítő modelljébe</span><span class="sxs-lookup"><span data-stu-id="acaa1-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="acaa1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acaa1-112">PARAMETERS</span></span>

### <span data-ttu-id="acaa1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="acaa1-113">-Force</span></span>
<span data-ttu-id="acaa1-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="acaa1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="acaa1-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="acaa1-115">-Location</span></span>
<span data-ttu-id="acaa1-116">Annak az Azure-helynek a neve, ahol a ExpressRoute-áramkör lakik.</span><span class="sxs-lookup"><span data-stu-id="acaa1-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="acaa1-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acaa1-117">-Name</span></span>
<span data-ttu-id="acaa1-118">Az áthelyezni kívánt ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="acaa1-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="acaa1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acaa1-119">-ResourceGroupName</span></span>
<span data-ttu-id="acaa1-120">Annak az erőforráscsoportnek a neve, amely a ExpressRoute-áramkör áthelyezését fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="acaa1-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="acaa1-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="acaa1-121">-ServiceKey</span></span>
<span data-ttu-id="acaa1-122">A klasszikus telepítő modell ExpressRoute áramköre által használt szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="acaa1-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="acaa1-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="acaa1-123">-Tag</span></span>
<span data-ttu-id="acaa1-124">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="acaa1-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="acaa1-125">Példa:</span><span class="sxs-lookup"><span data-stu-id="acaa1-125">For example:</span></span>

<span data-ttu-id="acaa1-126">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="acaa1-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="acaa1-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="acaa1-127">-Confirm</span></span>
<span data-ttu-id="acaa1-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="acaa1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acaa1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acaa1-129">-WhatIf</span></span>
<span data-ttu-id="acaa1-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="acaa1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acaa1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="acaa1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acaa1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acaa1-132">-DefaultProfile</span></span>
<span data-ttu-id="acaa1-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acaa1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acaa1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acaa1-134">CommonParameters</span></span>
<span data-ttu-id="acaa1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acaa1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acaa1-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acaa1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acaa1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acaa1-137">INPUTS</span></span>

## <span data-ttu-id="acaa1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acaa1-138">OUTPUTS</span></span>

### <span data-ttu-id="acaa1-139">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="acaa1-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acaa1-140">NOTES</span></span>

## <span data-ttu-id="acaa1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acaa1-141">RELATED LINKS</span></span>

[<span data-ttu-id="acaa1-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="acaa1-143">Új – AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="acaa1-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="acaa1-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="acaa1-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
