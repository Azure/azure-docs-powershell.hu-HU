---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186901"
---
# <span data-ttu-id="8e2df-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="8e2df-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="8e2df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e2df-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2df-103">Adott virtuális útválasztó-társ által megismert útvonalak listája</span><span class="sxs-lookup"><span data-stu-id="8e2df-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="8e2df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e2df-104">SYNTAX</span></span>

### <span data-ttu-id="8e2df-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e2df-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e2df-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e2df-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e2df-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e2df-107">DESCRIPTION</span></span>
<span data-ttu-id="8e2df-108">Felsorolhatja azokat az útvonalakat, amelyeket a virtuális útválasztó-partnerek más forrásokból is megismertek.</span><span class="sxs-lookup"><span data-stu-id="8e2df-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="8e2df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e2df-109">EXAMPLES</span></span>

### <span data-ttu-id="8e2df-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e2df-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="8e2df-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="8e2df-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="8e2df-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e2df-112">PARAMETERS</span></span>

### <span data-ttu-id="8e2df-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e2df-113">-AsJob</span></span>
<span data-ttu-id="8e2df-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8e2df-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e2df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2df-115">-DefaultProfile</span></span>
<span data-ttu-id="8e2df-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e2df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2df-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e2df-117">-InputObject</span></span>
<span data-ttu-id="8e2df-118">A virtuális útválasztó társközi beviteli objektuma.</span><span class="sxs-lookup"><span data-stu-id="8e2df-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="8e2df-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8e2df-119">-PeerName</span></span>
<span data-ttu-id="8e2df-120">Virtuális útválasztó-társ neve</span><span class="sxs-lookup"><span data-stu-id="8e2df-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="8e2df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2df-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e2df-122">A virtuális útválasztó társközi erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8e2df-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="8e2df-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="8e2df-123">-VirtualRouterName</span></span>
<span data-ttu-id="8e2df-124">Virtuális útválasztó neve</span><span class="sxs-lookup"><span data-stu-id="8e2df-124">Virtual router name</span></span>

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

### <span data-ttu-id="8e2df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2df-125">CommonParameters</span></span>
<span data-ttu-id="8e2df-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e2df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2df-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e2df-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2df-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2df-128">INPUTS</span></span>

### <span data-ttu-id="8e2df-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8e2df-129">System.String</span></span>

### <span data-ttu-id="8e2df-130">Microsoft. Azure. commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8e2df-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="8e2df-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e2df-131">OUTPUTS</span></span>

### <span data-ttu-id="8e2df-132">Microsoft. Azure. commands. Network. models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="8e2df-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="8e2df-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e2df-133">NOTES</span></span>

## <span data-ttu-id="8e2df-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e2df-134">RELATED LINKS</span></span>