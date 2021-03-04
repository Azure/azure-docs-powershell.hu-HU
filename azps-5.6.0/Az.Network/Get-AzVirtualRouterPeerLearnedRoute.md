---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 99f76a12afdbc883d990fff5a05e06e2880aecf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935666"
---
# <span data-ttu-id="2f52d-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="2f52d-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="2f52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f52d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f52d-103">List routes learned by a specific virtual router peer</span><span class="sxs-lookup"><span data-stu-id="2f52d-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="2f52d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f52d-104">SYNTAX</span></span>

### <span data-ttu-id="2f52d-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f52d-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f52d-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f52d-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f52d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f52d-107">DESCRIPTION</span></span>
<span data-ttu-id="2f52d-108">Számba veszi egy virtuális útválasztó-társ által más forrásokból tanult útvonalakat.</span><span class="sxs-lookup"><span data-stu-id="2f52d-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="2f52d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f52d-109">EXAMPLES</span></span>

### <span data-ttu-id="2f52d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2f52d-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="2f52d-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="2f52d-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="2f52d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f52d-112">PARAMETERS</span></span>

### <span data-ttu-id="2f52d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f52d-113">-AsJob</span></span>
<span data-ttu-id="2f52d-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2f52d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f52d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f52d-115">-DefaultProfile</span></span>
<span data-ttu-id="2f52d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f52d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f52d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f52d-117">-InputObject</span></span>
<span data-ttu-id="2f52d-118">A virtuális útválasztó társ bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="2f52d-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="2f52d-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2f52d-119">-PeerName</span></span>
<span data-ttu-id="2f52d-120">Virtuális útválasztó-társnév</span><span class="sxs-lookup"><span data-stu-id="2f52d-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="2f52d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f52d-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f52d-122">Virtuális útválasztó-társerőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="2f52d-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="2f52d-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="2f52d-123">-VirtualRouterName</span></span>
<span data-ttu-id="2f52d-124">Virtuális útválasztó neve</span><span class="sxs-lookup"><span data-stu-id="2f52d-124">Virtual router name</span></span>

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

### <span data-ttu-id="2f52d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f52d-125">CommonParameters</span></span>
<span data-ttu-id="2f52d-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f52d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f52d-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f52d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f52d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f52d-128">INPUTS</span></span>

### <span data-ttu-id="2f52d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2f52d-129">System.String</span></span>

### <span data-ttu-id="2f52d-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2f52d-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="2f52d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f52d-131">OUTPUTS</span></span>

### <span data-ttu-id="2f52d-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="2f52d-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="2f52d-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f52d-133">NOTES</span></span>

## <span data-ttu-id="2f52d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f52d-134">RELATED LINKS</span></span>
