---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379566"
---
# <span data-ttu-id="7117f-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7117f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7117f-102">SYNOPSIS</span></span>
<span data-ttu-id="7117f-103">Áthelyez egy ExpressRoute-áramkört a klasszikus telepítési modellről az Erőforrás-kezelő telepítési modellbe.</span><span class="sxs-lookup"><span data-stu-id="7117f-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="7117f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7117f-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7117f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7117f-105">DESCRIPTION</span></span>
<span data-ttu-id="7117f-106">A **Move-AzExpressRouteCircuit** parancsmag áthelyez egy ExpressRoute-áramkört a klasszikus telepítési modellről az Erőforrás-kezelő telepítési modellbe.</span><span class="sxs-lookup"><span data-stu-id="7117f-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="7117f-107">Az áthelyezés után az ExpressRoute-áramkör ugyanúgy viselkedik és teljesít, mint bármely más, az Erőforrás-kezelő telepítési modellben létrehozott ExpressRoute-áramkör.</span><span class="sxs-lookup"><span data-stu-id="7117f-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="7117f-108">Ez a művelet nem lépi át az áramköri kapcsolatokat, a virtuális hálózatokat és a VPN-átjárókat.</span><span class="sxs-lookup"><span data-stu-id="7117f-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="7117f-109">Ezeket az erőforrásokat az áthelyezés után újra kell konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="7117f-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="7117f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7117f-110">EXAMPLES</span></span>

### <span data-ttu-id="7117f-111">1. példa: ExpressRoute-áramkör áthelyezése az Erőforrás-kezelő telepítési modellbe</span><span class="sxs-lookup"><span data-stu-id="7117f-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="7117f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7117f-112">PARAMETERS</span></span>

### <span data-ttu-id="7117f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7117f-113">-AsJob</span></span>
<span data-ttu-id="7117f-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7117f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7117f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7117f-115">-DefaultProfile</span></span>
<span data-ttu-id="7117f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7117f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7117f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7117f-117">-Force</span></span>
<span data-ttu-id="7117f-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7117f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7117f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7117f-119">-Location</span></span>
<span data-ttu-id="7117f-120">Annak az Azure-helynek a neve, ahol az ExpressRoute-áramkör található.</span><span class="sxs-lookup"><span data-stu-id="7117f-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="7117f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7117f-121">-Name</span></span>
<span data-ttu-id="7117f-122">Az áthelyezni megfelelő ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="7117f-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="7117f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7117f-123">-ResourceGroupName</span></span>
<span data-ttu-id="7117f-124">Annak az erőforráscsoportnak a neve, amely az áthelyezett ExpressRoute-áramkört fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="7117f-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="7117f-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="7117f-125">-ServiceKey</span></span>
<span data-ttu-id="7117f-126">Az ExpressRoute-áramkör által használt szolgáltatáskulcs a klasszikus telepítési modellben.</span><span class="sxs-lookup"><span data-stu-id="7117f-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="7117f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="7117f-127">-Tag</span></span>
<span data-ttu-id="7117f-128">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="7117f-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7117f-129">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="7117f-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7117f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7117f-130">-Confirm</span></span>
<span data-ttu-id="7117f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7117f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7117f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7117f-132">-WhatIf</span></span>
<span data-ttu-id="7117f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7117f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7117f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7117f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7117f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7117f-135">CommonParameters</span></span>
<span data-ttu-id="7117f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7117f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7117f-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7117f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7117f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7117f-138">INPUTS</span></span>

### <span data-ttu-id="7117f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7117f-139">System.String</span></span>

### <span data-ttu-id="7117f-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7117f-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7117f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7117f-141">OUTPUTS</span></span>

### <span data-ttu-id="7117f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7117f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7117f-143">NOTES</span></span>

## <span data-ttu-id="7117f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7117f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7117f-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7117f-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7117f-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="7117f-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7117f-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
