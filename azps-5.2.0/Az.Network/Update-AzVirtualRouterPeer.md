---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350741"
---
# <span data-ttu-id="8f6ed-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8f6ed-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="8f6ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6ed-103">Társ frissítése Azure VirtualRouterben</span><span class="sxs-lookup"><span data-stu-id="8f6ed-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="8f6ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f6ed-104">SYNTAX</span></span>

### <span data-ttu-id="8f6ed-105">VirtualRouterNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f6ed-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6ed-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f6ed-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f6ed-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f6ed-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6ed-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f6ed-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6ed-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f6ed-109">DESCRIPTION</span></span>
<span data-ttu-id="8f6ed-110">Az **Update-AzVirtualRouterPeer** parancsmag egy VirtualRouter-társ frissítését egy Azure VirtualRouterre</span><span class="sxs-lookup"><span data-stu-id="8f6ed-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="8f6ed-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f6ed-111">EXAMPLES</span></span>

### <span data-ttu-id="8f6ed-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ed-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8f6ed-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ed-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8f6ed-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="8f6ed-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="8f6ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f6ed-115">PARAMETERS</span></span>

### <span data-ttu-id="8f6ed-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f6ed-116">-AsJob</span></span>
<span data-ttu-id="8f6ed-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8f6ed-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f6ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6ed-118">-DefaultProfile</span></span>
<span data-ttu-id="8f6ed-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6ed-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8f6ed-120">-Force</span></span>
<span data-ttu-id="8f6ed-121">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="8f6ed-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8f6ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6ed-122">-InputObject</span></span>
<span data-ttu-id="8f6ed-123">A virtuális útválasztó társ bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="8f6ed-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8f6ed-124">-PeerAsn</span></span>
<span data-ttu-id="8f6ed-125">Társközi ASN.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-125">Peer ASN.</span></span>

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

### <span data-ttu-id="8f6ed-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="8f6ed-126">-PeerIp</span></span>
<span data-ttu-id="8f6ed-127">Társ ip-címe.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-127">Peer Ip.</span></span>

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

### <span data-ttu-id="8f6ed-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8f6ed-128">-PeerName</span></span>
<span data-ttu-id="8f6ed-129">A virtuális társ útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="8f6ed-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6ed-130">-ResourceGroupName</span></span>
<span data-ttu-id="8f6ed-131">A virtuális útválasztó/társ erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="8f6ed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6ed-132">-ResourceId</span></span>
<span data-ttu-id="8f6ed-133">A virtuális útválasztó társerőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="8f6ed-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="8f6ed-134">-VirtualRouterName</span></span>
<span data-ttu-id="8f6ed-135">A virtuális útválasztó, ahol a társ létezik.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="8f6ed-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f6ed-136">-Confirm</span></span>
<span data-ttu-id="8f6ed-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6ed-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6ed-138">-WhatIf</span></span>
<span data-ttu-id="8f6ed-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6ed-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6ed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6ed-141">CommonParameters</span></span>
<span data-ttu-id="8f6ed-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6ed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6ed-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f6ed-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6ed-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f6ed-144">INPUTS</span></span>

### <span data-ttu-id="8f6ed-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8f6ed-145">System.String</span></span>

### <span data-ttu-id="8f6ed-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="8f6ed-146">System.UInt32</span></span>

### <span data-ttu-id="8f6ed-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8f6ed-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="8f6ed-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6ed-148">OUTPUTS</span></span>

### <span data-ttu-id="8f6ed-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8f6ed-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8f6ed-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f6ed-150">NOTES</span></span>

## <span data-ttu-id="8f6ed-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f6ed-151">RELATED LINKS</span></span>
