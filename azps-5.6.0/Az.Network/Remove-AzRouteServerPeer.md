---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: 52733af41b5f8d84811f1c1f184181a2d45053e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933770"
---
# <span data-ttu-id="7b5e0-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="7b5e0-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="7b5e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5e0-103">Eltávolít egy társt egy Azure RouteServer-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="7b5e0-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="7b5e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b5e0-104">SYNTAX</span></span>

### <span data-ttu-id="7b5e0-105">RouteServerNPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b5e0-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e0-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b5e0-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b5e0-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b5e0-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b5e0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b5e0-108">DESCRIPTION</span></span>
<span data-ttu-id="7b5e0-109">A **Remove-AzRouteServerPeer** parancsmag eltávolít egy RouteServer-társt egy Azure RouteServer-kiszolgálóról</span><span class="sxs-lookup"><span data-stu-id="7b5e0-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="7b5e0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b5e0-110">EXAMPLES</span></span>

### <span data-ttu-id="7b5e0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7b5e0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="7b5e0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="7b5e0-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="7b5e0-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="7b5e0-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="7b5e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b5e0-114">PARAMETERS</span></span>

### <span data-ttu-id="7b5e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b5e0-115">-AsJob</span></span>
<span data-ttu-id="7b5e0-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7b5e0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b5e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5e0-117">-DefaultProfile</span></span>
<span data-ttu-id="7b5e0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5e0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7b5e0-119">-Force</span></span>
<span data-ttu-id="7b5e0-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="7b5e0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7b5e0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b5e0-121">-InputObject</span></span>
<span data-ttu-id="7b5e0-122">Az útvonal-kiszolgáló társviszony-bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7b5e0-123">-PeerName</span></span>
<span data-ttu-id="7b5e0-124">Az útválasztási kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-124">The name of the route server Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b5e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b5e0-126">Az útvonal-kiszolgáló/társ erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-126">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b5e0-127">-ResourceId</span></span>
<span data-ttu-id="7b5e0-128">Az útvonalkiszolgáló társerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-128">The route server peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="7b5e0-129">-RouteServerName</span></span>
<span data-ttu-id="7b5e0-130">Az az útvonal-kiszolgáló, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-130">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b5e0-131">-Confirm</span></span>
<span data-ttu-id="7b5e0-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b5e0-133">-WhatIf</span></span>
<span data-ttu-id="7b5e0-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b5e0-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5e0-136">CommonParameters</span></span>
<span data-ttu-id="7b5e0-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5e0-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b5e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5e0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b5e0-139">INPUTS</span></span>

### <span data-ttu-id="7b5e0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7b5e0-140">System.String</span></span>

### <span data-ttu-id="7b5e0-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="7b5e0-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="7b5e0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b5e0-142">OUTPUTS</span></span>

### <span data-ttu-id="7b5e0-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="7b5e0-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="7b5e0-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b5e0-144">NOTES</span></span>

## <span data-ttu-id="7b5e0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b5e0-145">RELATED LINKS</span></span>
