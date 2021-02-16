---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 79d907a5ac1b75bdc65d6ea79ffc6c9dea911479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160531"
---
# <span data-ttu-id="2731c-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2731c-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="2731c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2731c-102">SYNOPSIS</span></span>
<span data-ttu-id="2731c-103">Társ frissítése Azure RouteServer-rekordban</span><span class="sxs-lookup"><span data-stu-id="2731c-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="2731c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2731c-104">SYNTAX</span></span>

### <span data-ttu-id="2731c-105">RouteServerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2731c-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2731c-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2731c-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2731c-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2731c-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2731c-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2731c-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2731c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2731c-109">DESCRIPTION</span></span>
<span data-ttu-id="2731c-110">Az **Update-AzRouteServerPeer** parancsmag frissíti a RouteServer-társokat egy Azure RouteServer-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="2731c-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="2731c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2731c-111">EXAMPLES</span></span>

### <span data-ttu-id="2731c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2731c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2731c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2731c-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="2731c-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="2731c-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="2731c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2731c-115">PARAMETERS</span></span>

### <span data-ttu-id="2731c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2731c-116">-AsJob</span></span>
<span data-ttu-id="2731c-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2731c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2731c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2731c-118">-DefaultProfile</span></span>
<span data-ttu-id="2731c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2731c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2731c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2731c-120">-Force</span></span>
<span data-ttu-id="2731c-121">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="2731c-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2731c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2731c-122">-InputObject</span></span>
<span data-ttu-id="2731c-123">Az útvonal-kiszolgáló társviszony-bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="2731c-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="2731c-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2731c-124">-PeerAsn</span></span>
<span data-ttu-id="2731c-125">Távoli útválasztási kiszolgálói társ asn-neve.</span><span class="sxs-lookup"><span data-stu-id="2731c-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2731c-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="2731c-126">-PeerIp</span></span>
<span data-ttu-id="2731c-127">Távoli útválasztási kiszolgálói társ IP-címe.</span><span class="sxs-lookup"><span data-stu-id="2731c-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="2731c-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2731c-128">-PeerName</span></span>
<span data-ttu-id="2731c-129">Az útválasztási kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2731c-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="2731c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2731c-130">-ResourceGroupName</span></span>
<span data-ttu-id="2731c-131">Az útvonal-kiszolgáló/társ erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="2731c-131">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="2731c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2731c-132">-ResourceId</span></span>
<span data-ttu-id="2731c-133">Az útvonalkiszolgáló társerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2731c-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="2731c-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="2731c-134">-RouteServerName</span></span>
<span data-ttu-id="2731c-135">Az az útvonal-kiszolgáló, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="2731c-135">The route server where peer exists.</span></span>

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

### <span data-ttu-id="2731c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2731c-136">-Confirm</span></span>
<span data-ttu-id="2731c-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2731c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2731c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2731c-138">-WhatIf</span></span>
<span data-ttu-id="2731c-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2731c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2731c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2731c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2731c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2731c-141">CommonParameters</span></span>
<span data-ttu-id="2731c-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2731c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2731c-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2731c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2731c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2731c-144">INPUTS</span></span>

### <span data-ttu-id="2731c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2731c-145">System.String</span></span>

### <span data-ttu-id="2731c-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2731c-146">System.UInt32</span></span>

### <span data-ttu-id="2731c-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="2731c-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="2731c-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2731c-148">OUTPUTS</span></span>

### <span data-ttu-id="2731c-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="2731c-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="2731c-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2731c-150">NOTES</span></span>

## <span data-ttu-id="2731c-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2731c-151">RELATED LINKS</span></span>
