---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932505"
---
# <span data-ttu-id="c4dce-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="c4dce-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="c4dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4dce-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dce-103">Társ hozzáadása Azure RouteServer-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="c4dce-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="c4dce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4dce-104">SYNTAX</span></span>

### <span data-ttu-id="c4dce-105">RouteServerNPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4dce-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4dce-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4dce-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4dce-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4dce-107">DESCRIPTION</span></span>
<span data-ttu-id="c4dce-108">Az **Add-AzRouteServerPeer** parancsmag hozzáad egy RouteServer-társt egy Azure RouteServer-kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="c4dce-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="c4dce-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4dce-109">EXAMPLES</span></span>

### <span data-ttu-id="c4dce-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4dce-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="c4dce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4dce-111">PARAMETERS</span></span>

### <span data-ttu-id="c4dce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4dce-112">-AsJob</span></span>
<span data-ttu-id="c4dce-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c4dce-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4dce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dce-114">-DefaultProfile</span></span>
<span data-ttu-id="c4dce-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4dce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4dce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c4dce-116">-Force</span></span>
<span data-ttu-id="c4dce-117">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="c4dce-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c4dce-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c4dce-118">-PeerAsn</span></span>
<span data-ttu-id="c4dce-119">Távoli útválasztási kiszolgálói társ asn-neve.</span><span class="sxs-lookup"><span data-stu-id="c4dce-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dce-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="c4dce-120">-PeerIp</span></span>
<span data-ttu-id="c4dce-121">Távoli útválasztási kiszolgálói társ IP-címe.</span><span class="sxs-lookup"><span data-stu-id="c4dce-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="c4dce-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c4dce-122">-PeerName</span></span>
<span data-ttu-id="c4dce-123">Az útvonalkiszolgáló-társ neve.</span><span class="sxs-lookup"><span data-stu-id="c4dce-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="c4dce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4dce-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4dce-125">Az útvonal-kiszolgáló/társ erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="c4dce-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="c4dce-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="c4dce-126">-RouteServerName</span></span>
<span data-ttu-id="c4dce-127">Az az útvonal-kiszolgáló, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="c4dce-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4dce-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4dce-128">-Confirm</span></span>
<span data-ttu-id="c4dce-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4dce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4dce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4dce-130">-WhatIf</span></span>
<span data-ttu-id="c4dce-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4dce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4dce-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4dce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4dce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dce-133">CommonParameters</span></span>
<span data-ttu-id="c4dce-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4dce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dce-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4dce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dce-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4dce-136">INPUTS</span></span>

### <span data-ttu-id="c4dce-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c4dce-137">System.String</span></span>

### <span data-ttu-id="c4dce-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="c4dce-138">System.UInt32</span></span>

## <span data-ttu-id="c4dce-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4dce-139">OUTPUTS</span></span>

### <span data-ttu-id="c4dce-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="c4dce-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="c4dce-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4dce-141">NOTES</span></span>

## <span data-ttu-id="c4dce-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4dce-142">RELATED LINKS</span></span>
