---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: aae01212b44eebf03207f2b0bfed788992acbc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015077"
---
# <span data-ttu-id="ce8fc-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="ce8fc-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="ce8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8fc-103">List routes being advertised by specific virtual router peer</span><span class="sxs-lookup"><span data-stu-id="ce8fc-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="ce8fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce8fc-104">SYNTAX</span></span>

### <span data-ttu-id="ce8fc-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce8fc-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8fc-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce8fc-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce8fc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce8fc-107">DESCRIPTION</span></span>
<span data-ttu-id="ce8fc-108">Egy adott virtuális útválasztó név vagy objektum szerint is felsorolja az adott társnak egy adott virtuális útválasztó által meghirdetett útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="ce8fc-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="ce8fc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce8fc-109">EXAMPLES</span></span>

### <span data-ttu-id="ce8fc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ce8fc-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="ce8fc-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ce8fc-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="ce8fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce8fc-112">PARAMETERS</span></span>

### <span data-ttu-id="ce8fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce8fc-113">-AsJob</span></span>
<span data-ttu-id="ce8fc-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ce8fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce8fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8fc-115">-DefaultProfile</span></span>
<span data-ttu-id="ce8fc-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce8fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce8fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce8fc-117">-InputObject</span></span>
<span data-ttu-id="ce8fc-118">A virtuális útválasztó társ bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="ce8fc-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8fc-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ce8fc-119">-PeerName</span></span>
<span data-ttu-id="ce8fc-120">Virtuális útválasztó-társnév</span><span class="sxs-lookup"><span data-stu-id="ce8fc-120">Virtual router peer name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce8fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce8fc-122">Virtuális útválasztó-társerőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="ce8fc-122">Virtual router peer resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8fc-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="ce8fc-123">-VirtualRouterName</span></span>
<span data-ttu-id="ce8fc-124">Virtuális útválasztó neve</span><span class="sxs-lookup"><span data-stu-id="ce8fc-124">Virtual router name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8fc-125">CommonParameters</span></span>
<span data-ttu-id="ce8fc-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8fc-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce8fc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8fc-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce8fc-128">INPUTS</span></span>

### <span data-ttu-id="ce8fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ce8fc-129">System.String</span></span>

### <span data-ttu-id="ce8fc-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ce8fc-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="ce8fc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce8fc-131">OUTPUTS</span></span>

### <span data-ttu-id="ce8fc-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="ce8fc-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="ce8fc-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce8fc-133">NOTES</span></span>

## <span data-ttu-id="ce8fc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce8fc-134">RELATED LINKS</span></span>
