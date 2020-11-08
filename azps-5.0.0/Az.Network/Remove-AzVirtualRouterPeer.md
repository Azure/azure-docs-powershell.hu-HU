---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186073"
---
# <span data-ttu-id="78de9-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="78de9-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="78de9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78de9-102">SYNOPSIS</span></span>
<span data-ttu-id="78de9-103">Társközi VirtualRouter eltávolítása</span><span class="sxs-lookup"><span data-stu-id="78de9-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="78de9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78de9-104">SYNTAX</span></span>

### <span data-ttu-id="78de9-105">VirtualRouterPeerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78de9-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78de9-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78de9-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78de9-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78de9-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78de9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="78de9-108">DESCRIPTION</span></span>
<span data-ttu-id="78de9-109">A **Remove-AzVirtualRouterPeer** parancsmag VirtualRouter-társközi eltávolítása egy Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="78de9-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="78de9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="78de9-110">EXAMPLES</span></span>

### <span data-ttu-id="78de9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="78de9-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="78de9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="78de9-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="78de9-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="78de9-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="78de9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78de9-114">PARAMETERS</span></span>

### <span data-ttu-id="78de9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78de9-115">-AsJob</span></span>
<span data-ttu-id="78de9-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="78de9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78de9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78de9-117">-DefaultProfile</span></span>
<span data-ttu-id="78de9-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78de9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78de9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78de9-119">-Force</span></span>
<span data-ttu-id="78de9-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78de9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78de9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78de9-121">-InputObject</span></span>
<span data-ttu-id="78de9-122">A virtuális útválasztó társközi beviteli objektuma.</span><span class="sxs-lookup"><span data-stu-id="78de9-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="78de9-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="78de9-123">-PeerName</span></span>
<span data-ttu-id="78de9-124">A virtuális útválasztó társközi neve.</span><span class="sxs-lookup"><span data-stu-id="78de9-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="78de9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78de9-125">-ResourceGroupName</span></span>
<span data-ttu-id="78de9-126">A virtuális útválasztó/társ erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="78de9-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="78de9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78de9-127">-ResourceId</span></span>
<span data-ttu-id="78de9-128">A virtuális útválasztó társközi erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78de9-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="78de9-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="78de9-129">-VirtualRouterName</span></span>
<span data-ttu-id="78de9-130">A virtuális útválasztó, ahol a társközi létezik.</span><span class="sxs-lookup"><span data-stu-id="78de9-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="78de9-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78de9-131">-Confirm</span></span>
<span data-ttu-id="78de9-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78de9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78de9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78de9-133">-WhatIf</span></span>
<span data-ttu-id="78de9-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78de9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78de9-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78de9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78de9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78de9-136">CommonParameters</span></span>
<span data-ttu-id="78de9-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78de9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78de9-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78de9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78de9-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78de9-139">INPUTS</span></span>

### <span data-ttu-id="78de9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78de9-140">System.String</span></span>

### <span data-ttu-id="78de9-141">Microsoft. Azure. commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="78de9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="78de9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78de9-142">OUTPUTS</span></span>

### <span data-ttu-id="78de9-143">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="78de9-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="78de9-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78de9-144">NOTES</span></span>

## <span data-ttu-id="78de9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78de9-145">RELATED LINKS</span></span>