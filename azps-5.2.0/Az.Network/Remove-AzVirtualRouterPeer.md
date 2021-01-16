---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365481"
---
# <span data-ttu-id="94f74-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="94f74-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="94f74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f74-102">SYNOPSIS</span></span>
<span data-ttu-id="94f74-103">Egy Azure VirtualRouter-társ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="94f74-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="94f74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94f74-104">SYNTAX</span></span>

### <span data-ttu-id="94f74-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94f74-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f74-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94f74-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f74-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94f74-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f74-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94f74-108">DESCRIPTION</span></span>
<span data-ttu-id="94f74-109">A **Remove-AzVirtualRouterPeer** parancsmag eltávolítja a VirtualRouter-társokat az Azure VirtualRouter-ból</span><span class="sxs-lookup"><span data-stu-id="94f74-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="94f74-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94f74-110">EXAMPLES</span></span>

### <span data-ttu-id="94f74-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="94f74-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="94f74-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="94f74-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="94f74-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="94f74-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="94f74-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f74-114">PARAMETERS</span></span>

### <span data-ttu-id="94f74-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f74-115">-AsJob</span></span>
<span data-ttu-id="94f74-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="94f74-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f74-117">-DefaultProfile</span></span>
<span data-ttu-id="94f74-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94f74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f74-119">-Force</span><span class="sxs-lookup"><span data-stu-id="94f74-119">-Force</span></span>
<span data-ttu-id="94f74-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="94f74-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="94f74-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f74-121">-InputObject</span></span>
<span data-ttu-id="94f74-122">A virtuális útválasztó társ bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="94f74-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="94f74-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="94f74-123">-PeerName</span></span>
<span data-ttu-id="94f74-124">A virtuális társ útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="94f74-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="94f74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f74-125">-ResourceGroupName</span></span>
<span data-ttu-id="94f74-126">A virtuális útválasztó/társ erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="94f74-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="94f74-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94f74-127">-ResourceId</span></span>
<span data-ttu-id="94f74-128">A virtuális útválasztó társerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94f74-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="94f74-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="94f74-129">-VirtualRouterName</span></span>
<span data-ttu-id="94f74-130">A virtuális útválasztó, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="94f74-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="94f74-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94f74-131">-Confirm</span></span>
<span data-ttu-id="94f74-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="94f74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f74-133">-WhatIf</span></span>
<span data-ttu-id="94f74-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="94f74-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f74-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94f74-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f74-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f74-136">CommonParameters</span></span>
<span data-ttu-id="94f74-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f74-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f74-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94f74-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f74-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94f74-139">INPUTS</span></span>

### <span data-ttu-id="94f74-140">System.String</span><span class="sxs-lookup"><span data-stu-id="94f74-140">System.String</span></span>

### <span data-ttu-id="94f74-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="94f74-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="94f74-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f74-142">OUTPUTS</span></span>

### <span data-ttu-id="94f74-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="94f74-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="94f74-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94f74-144">NOTES</span></span>

## <span data-ttu-id="94f74-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94f74-145">RELATED LINKS</span></span>
