---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: 0d798c5eb70c8c472862e9af0f992d01827a750e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919650"
---
# <span data-ttu-id="39446-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="39446-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="39446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39446-102">SYNOPSIS</span></span>
<span data-ttu-id="39446-103">RouteServer-társ be van ásva egy Azure RouteServer-kiszolgálóban</span><span class="sxs-lookup"><span data-stu-id="39446-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="39446-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39446-104">SYNTAX</span></span>

### <span data-ttu-id="39446-105">RouteServerNPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39446-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39446-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39446-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39446-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39446-107">DESCRIPTION</span></span>
<span data-ttu-id="39446-108">A **Get-AzRouteServerPeer** parancsmag egy Azure RouteServer-kiszolgálóhoz kap egy társt</span><span class="sxs-lookup"><span data-stu-id="39446-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="39446-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39446-109">EXAMPLES</span></span>

### <span data-ttu-id="39446-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="39446-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="39446-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="39446-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="39446-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39446-112">PARAMETERS</span></span>

### <span data-ttu-id="39446-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39446-113">-DefaultProfile</span></span>
<span data-ttu-id="39446-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39446-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39446-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="39446-115">-PeerName</span></span>
<span data-ttu-id="39446-116">Az útvonalkiszolgáló-társ neve.</span><span class="sxs-lookup"><span data-stu-id="39446-116">The name of the route server peer.</span></span>

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

### <span data-ttu-id="39446-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39446-117">-ResourceGroupName</span></span>
<span data-ttu-id="39446-118">Az útvonal-kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="39446-118">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="39446-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39446-119">-ResourceId</span></span>
<span data-ttu-id="39446-120">Az útvonalkiszolgáló-társ Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="39446-120">ResourceId of the route server peer.</span></span>

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

### <span data-ttu-id="39446-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="39446-121">-RouteServerName</span></span>
<span data-ttu-id="39446-122">Az útvonalkiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="39446-122">The name of the route server.</span></span>

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

### <span data-ttu-id="39446-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39446-123">CommonParameters</span></span>
<span data-ttu-id="39446-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39446-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39446-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39446-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39446-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39446-126">INPUTS</span></span>

### <span data-ttu-id="39446-127">System.String</span><span class="sxs-lookup"><span data-stu-id="39446-127">System.String</span></span>

## <span data-ttu-id="39446-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39446-128">OUTPUTS</span></span>

### <span data-ttu-id="39446-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="39446-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="39446-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39446-130">NOTES</span></span>

## <span data-ttu-id="39446-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39446-131">RELATED LINKS</span></span>
