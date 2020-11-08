---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186903"
---
# <span data-ttu-id="9c43a-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9c43a-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="9c43a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c43a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c43a-103">VirtualRouter-társ bevonása Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="9c43a-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="9c43a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c43a-104">SYNTAX</span></span>

### <span data-ttu-id="9c43a-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c43a-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c43a-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c43a-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c43a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c43a-107">DESCRIPTION</span></span>
<span data-ttu-id="9c43a-108">A **Get-AzVirtualRouterPeer** parancsmag egy társközi VirtualRouter kap</span><span class="sxs-lookup"><span data-stu-id="9c43a-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="9c43a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9c43a-109">EXAMPLES</span></span>

### <span data-ttu-id="9c43a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c43a-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="9c43a-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="9c43a-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="9c43a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c43a-112">PARAMETERS</span></span>

### <span data-ttu-id="9c43a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c43a-113">-DefaultProfile</span></span>
<span data-ttu-id="9c43a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c43a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c43a-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="9c43a-115">-PeerName</span></span>
<span data-ttu-id="9c43a-116">A virtuális útválasztó társközi neve.</span><span class="sxs-lookup"><span data-stu-id="9c43a-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="9c43a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c43a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9c43a-118">A virtuális útválasztó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c43a-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="9c43a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c43a-119">-ResourceId</span></span>
<span data-ttu-id="9c43a-120">A virtuális útválasztó ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c43a-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="9c43a-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="9c43a-121">-VirtualRouterName</span></span>
<span data-ttu-id="9c43a-122">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="9c43a-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="9c43a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c43a-123">CommonParameters</span></span>
<span data-ttu-id="9c43a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c43a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c43a-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9c43a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c43a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c43a-126">INPUTS</span></span>

### <span data-ttu-id="9c43a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9c43a-127">System.String</span></span>

## <span data-ttu-id="9c43a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c43a-128">OUTPUTS</span></span>

### <span data-ttu-id="9c43a-129">Microsoft. Azure. commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="9c43a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="9c43a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c43a-130">NOTES</span></span>

## <span data-ttu-id="9c43a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c43a-131">RELATED LINKS</span></span>
