---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025129"
---
# <span data-ttu-id="c7c6f-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c7c6f-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="c7c6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c6f-103">Társközi frissítés egy Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c7c6f-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="c7c6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7c6f-104">SYNTAX</span></span>

### <span data-ttu-id="c7c6f-105">VirtualRouterNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7c6f-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c6f-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c6f-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7c6f-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c6f-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c6f-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c6f-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c6f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7c6f-109">DESCRIPTION</span></span>
<span data-ttu-id="c7c6f-110">Az **Update-AzVirtualRouterPeer parancsmag egy VirtualRouter-társközi webhelyre** frissíti az Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c7c6f-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="c7c6f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c7c6f-111">EXAMPLES</span></span>

### <span data-ttu-id="c7c6f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7c6f-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="c7c6f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c7c6f-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="c7c6f-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c7c6f-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="c7c6f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7c6f-115">PARAMETERS</span></span>

### <span data-ttu-id="c7c6f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7c6f-116">-AsJob</span></span>
<span data-ttu-id="c7c6f-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c7c6f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7c6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c6f-118">-DefaultProfile</span></span>
<span data-ttu-id="c7c6f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c6f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c7c6f-120">-Force</span></span>
<span data-ttu-id="c7c6f-121">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c7c6f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7c6f-122">-InputObject</span></span>
<span data-ttu-id="c7c6f-123">A virtuális útválasztó társközi beviteli objektuma.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="c7c6f-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c7c6f-124">-PeerAsn</span></span>
<span data-ttu-id="c7c6f-125">Társközi ASN.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c6f-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="c7c6f-126">-PeerIp</span></span>
<span data-ttu-id="c7c6f-127">Társközi IP.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-127">Peer Ip.</span></span>

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

### <span data-ttu-id="c7c6f-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c7c6f-128">-PeerName</span></span>
<span data-ttu-id="c7c6f-129">A virtuális útválasztó társközi neve.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="c7c6f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c6f-130">-ResourceGroupName</span></span>
<span data-ttu-id="c7c6f-131">A virtuális útválasztó/társ erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="c7c6f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7c6f-132">-ResourceId</span></span>
<span data-ttu-id="c7c6f-133">A virtuális útválasztó társközi erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="c7c6f-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c7c6f-134">-VirtualRouterName</span></span>
<span data-ttu-id="c7c6f-135">A virtuális útválasztó, ahol a társközi létezik.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="c7c6f-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7c6f-136">-Confirm</span></span>
<span data-ttu-id="c7c6f-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c6f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c6f-138">-WhatIf</span></span>
<span data-ttu-id="c7c6f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c6f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c6f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c6f-141">CommonParameters</span></span>
<span data-ttu-id="c7c6f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7c6f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c6f-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c7c6f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c6f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c6f-144">INPUTS</span></span>

### <span data-ttu-id="c7c6f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c6f-145">System.String</span></span>

### <span data-ttu-id="c7c6f-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="c7c6f-146">System.UInt32</span></span>

### <span data-ttu-id="c7c6f-147">Microsoft. Azure. commands. Network. models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c7c6f-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c7c6f-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7c6f-148">OUTPUTS</span></span>

### <span data-ttu-id="c7c6f-149">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c7c6f-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="c7c6f-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7c6f-150">NOTES</span></span>

## <span data-ttu-id="c7c6f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7c6f-151">RELATED LINKS</span></span>
