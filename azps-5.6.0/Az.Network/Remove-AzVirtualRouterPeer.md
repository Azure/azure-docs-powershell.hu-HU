---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 2c88ac8c0f3f089a4a26bf0e29ec855281e7f8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005926"
---
# <span data-ttu-id="93765-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="93765-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="93765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93765-102">SYNOPSIS</span></span>
<span data-ttu-id="93765-103">Egy Azure VirtualRouter-társ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="93765-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="93765-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93765-104">SYNTAX</span></span>

### <span data-ttu-id="93765-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93765-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93765-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93765-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93765-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93765-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93765-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93765-108">DESCRIPTION</span></span>
<span data-ttu-id="93765-109">A **Remove-AzVirtualRouterPeer** parancsmag eltávolítja a VirtualRouter-társokat az Azure VirtualRouter-ból</span><span class="sxs-lookup"><span data-stu-id="93765-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="93765-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93765-110">EXAMPLES</span></span>

### <span data-ttu-id="93765-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="93765-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="93765-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="93765-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="93765-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="93765-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="93765-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93765-114">PARAMETERS</span></span>

### <span data-ttu-id="93765-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93765-115">-AsJob</span></span>
<span data-ttu-id="93765-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="93765-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93765-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93765-117">-DefaultProfile</span></span>
<span data-ttu-id="93765-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93765-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93765-119">-Force</span><span class="sxs-lookup"><span data-stu-id="93765-119">-Force</span></span>
<span data-ttu-id="93765-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="93765-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="93765-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93765-121">-InputObject</span></span>
<span data-ttu-id="93765-122">A virtuális útválasztó társ bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="93765-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="93765-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="93765-123">-PeerName</span></span>
<span data-ttu-id="93765-124">A virtuális társ útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="93765-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="93765-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93765-125">-ResourceGroupName</span></span>
<span data-ttu-id="93765-126">A virtuális útválasztó/társ erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="93765-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="93765-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93765-127">-ResourceId</span></span>
<span data-ttu-id="93765-128">A virtuális útválasztó társerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93765-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="93765-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="93765-129">-VirtualRouterName</span></span>
<span data-ttu-id="93765-130">A virtuális útválasztó, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="93765-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="93765-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93765-131">-Confirm</span></span>
<span data-ttu-id="93765-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="93765-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93765-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93765-133">-WhatIf</span></span>
<span data-ttu-id="93765-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="93765-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93765-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93765-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93765-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93765-136">CommonParameters</span></span>
<span data-ttu-id="93765-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93765-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93765-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93765-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93765-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93765-139">INPUTS</span></span>

### <span data-ttu-id="93765-140">System.String</span><span class="sxs-lookup"><span data-stu-id="93765-140">System.String</span></span>

### <span data-ttu-id="93765-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="93765-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="93765-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93765-142">OUTPUTS</span></span>

### <span data-ttu-id="93765-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="93765-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="93765-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93765-144">NOTES</span></span>

## <span data-ttu-id="93765-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93765-145">RELATED LINKS</span></span>
