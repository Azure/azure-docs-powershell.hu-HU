---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 7b17b124b7d4e0dc89ee7e61469b26401002db9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923986"
---
# <span data-ttu-id="10154-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="10154-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="10154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10154-102">SYNOPSIS</span></span>
<span data-ttu-id="10154-103">VirtualRouter-társ az Azure VirtualRouterben</span><span class="sxs-lookup"><span data-stu-id="10154-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="10154-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10154-104">SYNTAX</span></span>

### <span data-ttu-id="10154-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10154-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10154-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10154-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10154-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10154-107">DESCRIPTION</span></span>
<span data-ttu-id="10154-108">A **Get-AzVirtualRouterPeer** parancsmag kap egy társt egy Azure VirtualRouterben</span><span class="sxs-lookup"><span data-stu-id="10154-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="10154-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10154-109">EXAMPLES</span></span>

### <span data-ttu-id="10154-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="10154-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="10154-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="10154-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="10154-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10154-112">PARAMETERS</span></span>

### <span data-ttu-id="10154-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10154-113">-DefaultProfile</span></span>
<span data-ttu-id="10154-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10154-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10154-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="10154-115">-PeerName</span></span>
<span data-ttu-id="10154-116">A virtuális útválasztó-társ neve.</span><span class="sxs-lookup"><span data-stu-id="10154-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="10154-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10154-117">-ResourceGroupName</span></span>
<span data-ttu-id="10154-118">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="10154-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="10154-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10154-119">-ResourceId</span></span>
<span data-ttu-id="10154-120">A virtuális útválasztó ResourceId-neve.</span><span class="sxs-lookup"><span data-stu-id="10154-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10154-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="10154-121">-VirtualRouterName</span></span>
<span data-ttu-id="10154-122">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="10154-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="10154-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10154-123">CommonParameters</span></span>
<span data-ttu-id="10154-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10154-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10154-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10154-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10154-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10154-126">INPUTS</span></span>

### <span data-ttu-id="10154-127">System.String</span><span class="sxs-lookup"><span data-stu-id="10154-127">System.String</span></span>

## <span data-ttu-id="10154-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10154-128">OUTPUTS</span></span>

### <span data-ttu-id="10154-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="10154-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="10154-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10154-130">NOTES</span></span>

## <span data-ttu-id="10154-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10154-131">RELATED LINKS</span></span>
